Making an Audio-Reactive AI-generated Video: RunwayML and TouchDesigner
=====================================================
April 25, 2021

Lia Coleman
-------------
[Lia Coleman](https://www.liacoleman.com) is an AI artist and educator. She makes art with AI and teaches others how to do it.

**Sign up for her [AI Artwork Newsletter](https://makeaiart.substack.com/).**

Instagram: *[@liacole7](https://instagram.com/liacole7)*

Twitter: *[@lialialiacole](https://twitter.com/lialialiacole)*

## [Link to slides](https://docs.google.com/presentation/d/1cV0wFDm6t47Cgh37UO5u_nWuwvRmf6DQkmJxLdmZvd4/edit?usp=sharing)

## Recording on Youtube

## Description

Videos are so much cooler when they're synced up to music! And if you really wanna blow some minds you can use AI to generate the source video! 🤯

In this hands-on workshop, you'll learn how to make AI-generated videos in [RunwayML](https://runwayml.com), and also how to bring them into [TouchDesigner](https://derivative.ca/) to make them audio-reactive.

At the end of this workshop, you'll have:

- made your own AI-generated video that is synced up to a music track of your choice.
- learned how to build your own beat detector from scratch in TouchDesigner. This way, you can sync up any video to any audio track.
- learned a bit of machine learning in RunwayML along the way.

## Background

No prior experience necessary. To follow along:

1. Make an account on [RunwayML](https://runwayml.com).
2. Download [TouchDesigner](https://derivative.ca/)
3. Bring an .mp3 if you want to follow along!

## Schedule

- Intro, Setup
- Machine Learning primer, Intro to a Latent Space
- [RunwayML] Get an AI-generated Video
- break
- [TouchDesigner] Build a Beat Detector in TouchDesigner
- break
- [TouchDesigner] Hook up the beat detector to a video
- [TouchDesigner] Export the Video
- Sharing Work
- Fill out survey
- Resources to Explore More

# Steps

1. Get (an AI-generated) source video in RunwayML
2. Build a Beat detector
3. Hook it up to a video to control video playback speed
4. Exporting video

All of the TouchDesigner projects are saved out, step-by-step here: [**Link to Google Drive with Course Materials**](https://drive.google.com/drive/folders/10lgPA7BZU-TX4ScOHlmT8yV7ZcjMwJrl?usp=sharing)

# 1. Get (an AI-generated) source video in RunwayML

Go to [RunwayML](https://app.runwayml.com/). In the sidecar, click Models > Latent Video. Then pick a model you want to play with!

Once you have picked a model, click 'Export' in the bottom half window. This will take you to a different UI to Generate the Latent Walk Video.

Here, you can choose which 'keyframes' will be in the final interpolation video.

Tip: if you want to make a looping video, you can 

# 2. Building a Beat Detector

Our goal is to be able to take an MP3, and analyze the audio to detect the beats. 

IN: audio, mp3

OUT: a 0,1 signal when beats hit

1. Create a new project in TD.
2. Use TAB to open the operator menu in TouchDesigner. You'll be using this a lot!!
3. Add an Audio File IN. At this point, you can input your audio track of choice.
4. Add an Audio Dev OUT so we can hear what we're working with.
5. We only want one channel. Add MATH node with Combine Channels: Average. This will average the 2 channels into one!
6. Add Audiospect node. Shows Frequency spectrum of the song. Change High Frequency Boost to 1 for more control.
7. Add Analyze node. Function: Average. Just takes average of all inputs.

Thus far, we have the area under the curve at instantaneous moment in time. What we want is a digital {0,1} output.

8. Add a Trail node. This takes its input and shows the values over a time window. Set the Window length: 1s.  At this point, the peaks are what we want to extract. These are the kicks.

Now, we want to extract the peaks. We see we have values that are less than 0.10. First we're going to normalize the value to a value from 0.0 to 1.0. To normalize it:

1. This will come in handy later: Let's first use a Math node to multiply the values into more usable values between 0 and 100. Set Multiply = 1000.
2. To normalize the value, let's use a Limit node. Set Normalize = On. This will clamp the output to -1.0 to 1.0. 
3. Now, to cut off only the peaks, let's change in our Limit node the Type = Clamp. Then we can use this to truncate the signal. We only want values greater than min = 85 and max = 100. **This MINIMUM threshold value is really important when using different tracks to fine-tune.**

We now have the beats signal from -1.0 to 1.0. 

1. To normalize it from 0 to 1, we add a Math node. Then we set its Range > From Range: -1 to 1. To Range: 0 to 1.

Now, we notice that we have some things in the signal we need to fix. We notice that the peaks aren't the same height, and also that the length/width of each peak is different. To fix this, we add a Trigger node.

Now, to have it trigger on each peak, set Trigger > Trigger Threshold = 0.4.

To view, let's add a Trail node above it. This is just for us to see what's going on.

Now, we can see that in the Trail node, it looks a little irregular. What we can do about this in the Trail node: 

- Attack > Attack Length = 0. We can bring the attack all the way down.
- Attack > Peak Length = 0. We also bring down the Peak Length to 0 as well.
- Sustain > Decay Length = 0 as well.
- Sustain > Sustain Level = 1 (instead of 0.5).
- Sustain > Release Length = 0.

We see that these are now more snappy & instantaneous.

We can also add:

- Sustain > Min Sustain Length = 0.1 to get more of a square wave.

This is looking good! At this point, we can click the blue circle on the last Trigger node to view our results.

We see that we have some extra peaks here in this Trail node. What we can do about that is go back to the first Trail Node, and reduce the Window Length = 0.1s instead of 1s. This will be a little harder for us to see but it will make it snappier and not false-positive.

The two parameters that you will be adjusting for different songs are

THRESHOLD : Limit1 node, Limit > Minimum

MULTIPLY : Math2 node, Mult-Add > Multiply

Play with the threshold value and see what it controls. It just really truncates the peaks at different heights. The lower you make the threshold, the more peaks are be let through that will trigger.

**BONUS**: If you want to fine-tune on a specific portion of the audio signal, you can add a TRIM node after the Audiospect node. This is essentially an audio filter. For example, if you just wanted the highs of the song to trigger, you could 

- Trim > Start: set to % units. Start= 0.6%.
- Trim > End: set to % units. End = -0.2%.

Great, now that it's done— Make it into its own component!

### Making a Component

1. Create a Container node. This is under the COMP operator type. We've only been working with CHOPs thus far.
2. Drag and drop everything inside. 
3. Zoom in, and add an IN node and an OUT node (both CHOP nodes). 
4. Reconnect the audio file IN into the in of your new component. You can also rename it 'beatDetector' if you like.
5. Add a NULL chop so we can see our output.

# 3. Using the beat detector to control video

1. Add a video, by adding a Movie File In TOP. We can plug in any video here. You can plug in your AI-generated video from RunwayML earlier.

**NOTE: A longer video of 2-3 mins, or a looping video (it's easy to make a looping video) RunwayML works best,**

2. Turn Cue = On. We're going to use the "Cue Point" parameter in the Movie File In. We will use this to control which frame of the video is displayed. Try editing this value manually— you'll see that it literally controls what frame of the video is shown.

3. Let's first connect the null out from the BeatDetector to the Cue Point as a CHOP reference. 

We do this by turning off the Viewer mode in the Null node by clicking the little white in the bottom-right, then clicking and dragging the Null value to the Movie File In parameter window, and into the 'Cue Point' area. From the drop-down that appears, we select 'CHOP reference.' What "CHOP reference" means is that it is a live value that's tied in real-time to the active value. Whenever the output of the beat detector changes, the cue point will change. 

4. Now, what we want to do, is we have this value that is output that flashes between 0 and 1. What we want is a cumulatively increasing value, so we can scrub through all of the frames of the video, rather than just flashing between two frames. The CHOP that we want is a Speed. 

Let's add this Speed node between the BeatDetector and the output Null.

5. Optional: if we want to view the difference in signal, we can add a Trail node. Let's hook into the input of a new Trail node the output of the BeatDetector (digital), and also the output of the Speed node (cumulative).

If we go over to the Movie File In node and check on the active "Cue Point" value, we can see that it keeps incrementing upward with every hit.

6. Now, to have more control over the speed, we can add a Math node before the Speed node. This will have the effect of increasing the playback speed. 

- In the Math node, go to the Range tab. Here, change to To Range: to 0 to **10**. We can keep from range: 0 to 1. Changing the output will mean that it takes bigger steps.
- Also, it's only moving when the beat hits. Otherwise, the video playback at is 0. To fix this, we can add a minimum speed, by setting the bottom-value of the To Range: **1** to 10. Note: don't make this value under 1, because otherwise it will lag because it's trying to split up / interpolate between frames that you don't have.

7. It's already really great!! But if we want it to be a little bit smoother, we can add a Lag node. This will go after the Math node and before the Speed node. This will smooth out the signal. 

In the Lag node, let's add this to the Trail node so we can see what's happening here. (We can disconnect the Speed node for now.) Basically there's an attack and a release. Well, we don't want an attack because we want it to hit exactly on beat, so we set the lower Lag value to 0. We can leave the upper value to 0.2 here because we can see it's smoothly moving back to 0. 

Now if we reconnect the Speed node to the Trail node to check out what the signal looks like, we see that each of the steps is smoother, and less like a *step* step and more like a little smooth hump. Nice!

We can check the subtle impact of this Lag node by bypassing it on/off to see the difference.

8. To reset the video, go to the Speed node and click Speed > Reset: Pulse. This will reset the value of the Speed output to 0, which will set the Cue Point back to frame 0.

Video options:

- If you only want a trimmed section of the video: In the Speed Node you can go to Limit Type = Loop, and se the minimum & maximum values to set the trimmed portion of the video you want. 0 to 10 = 0 to 10s.

# 4. Exporting Video

1. Add a MovieFileOut TOP to the end. The input to this is the output of MovieFileIn (which is being driven by the BeatDetector).
2. Also we need to add Audio out as well. Otherwise we'll only export the video with no audio. So in the MovieFileOut's "Audio CHOP" parameter, let's click and drag the AudioDevOut there. Since TD is all python expressions, we see the pointer to the name of that Audio CHOP.
3. Click on the name of the parameter "File", and select the gray-white square all the way on the left. This is for a plain string value. (Otherwise the default is a Python expression.) You can click the + on the right too, to select where you want to save the file.
4. Click "Record" to record it.


### Support

This program is supported, in part, by public funds from the New York City Department of Cultural Affairs in partnership with the City Council. And by Babycastles members. Thank you.
