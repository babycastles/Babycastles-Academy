Introduction to Audio Synthesis with Machine Learning
=====================================================

Allan Pichardo
--------------

January 17, 2021

[Archived video](https://www.youtube.com/watch?v=MNAgKB-IFS4) on YouTube

[*allanpichardo.com*](https://allanpichardo.com/)

Instagram: [*@mylovemhz*](https://instagram.com/mylovemhz)

Twitter: [*@allanpichardo*](https://twitter.com/allanpichardo)

Introduction & Learning Goals
-----------------------------

In this workshop, we will cover the basic intuition behind the variational autoencoder–a basic generative model. We will use a variety of synth samples as training data and use the final trained decoder to output a range of random wav files of unique sounds that can be used in a sampler or DAW.

In this workshop, students will learn:

- Basic concepts behind variational autoencoders
- Basic concepts of digital audio and spectrograms
- How to build and train a generative model
- Use the trained model to generate and export unique sounds

Prerequisite / Background knowledge
-----------------------------------

No prior background in machine learning is necessary, however it is recommended that participants feel comfortable coding in Python. All datasets, tools, and environments will be provided in the form of a Google Colab notebook, so only a web browser is required.

Schedule / Suggested Duration
-----------------------------

- Variational Autoencoders: Basic Intuition \~10 min
- Spectrograms: Digital Audio Basics \~10 min
- Our Plan: An overview \~1 min
- Coding example \~1 hour
- Training the model \~15 minutes
- Generating Sounds \~30 minutes
- Questions \~15 minutes

Materials Needed / Planning Notes
---------------------------------

All teaching resources are available in the Github repo:

[*https://github.com/allanpichardo/vae\_synth*](https://github.com/allanpichardo/vae_synth)

Students should follow along with the Google Colab notebook:

[*https://colab.research.google.com/github/allanpichardo/audio-generation-autoencoder/blob/main/Audio\_Generation\_with\_Autoencoders.ipynb*](https://colab.research.google.com/github/allanpichardo/audio-generation-autoencoder/blob/main/Audio_Generation_with_Autoencoders.ipynb)

Link to slides / Resources
--------------------------

Slides are integrated into the notebook at: [*https://colab.research.google.com/github/allanpichardo/audio-generation-autoencoder/blob/main/Audio\_Generation\_with\_Autoencoders.ipynb*](https://colab.research.google.com/github/allanpichardo/audio-generation-autoencoder/blob/main/Audio_Generation_with_Autoencoders.ipynb)

Assessment
----------

What is a variational autoencoder?

What is a convolutional neural network?

What is a latent vector?

What property of a variational autoencoder enables the generation of new data?

Glossary 
---------

**Convolutional neural network** - In deep learning, a convolutional neural network is a class of deep neural networks, most commonly applied to analyzing visual imagery.

**Short-term Fourier Transform** - STFTs as well as standard Fourier transforms and other tools are frequently used to analyze music. The spectrogram can, for example, show frequency on the horizontal axis, with the lowest frequencies at left, and the highest at the right. The height of each bar (augmented by color) represents the amplitude of the frequencies within that band. The depth dimension represents time, where each new bar was a separate distinct transform.

Procedure
---------

The introduction will introduce students into basic concepts behind machine learning. This will be at a high level and not delve into the calculus. We will discuss linear functions as a basic example and how the composition of functions such as f(g(x)) can lead to more complex functions. This is the fundamental concept behind machine learning.

Secondly, we will discuss digital audio and how it’s represented in a computer. We will discuss spectrograms and how they represent audio waves as images.

Finally, the variational autoencoder will be introduced at a high level. We will focus on the “bottleneck” shape of the network and how it compresses complex information into simpler low-dimensional vectors.

Following the introduction, we will do a coding exercise where we will build and train a very basic autoencoder. Students will use the dataset provided to train the model and run the application Tensorboard to see the progression of the network during training.

At the end of the exercise, students will use the trained network to export and listen to random audio samples.

Student Reflections, Takeaways & Next Steps
-------------------------------------------

[*Autoencoding Neural Networks as Musical Audio Synthesizers*](https://ee.cooper.edu/~keene/assets/dafx2018_submission42_revised_jcolonel.pdf)

[*Kapre: On-GPU Audio Preprocessing Layers for a Quick Implementation of Deep Neural Network Models with Keras*](https://arxiv.org/abs/1706.05781)

*Thanks to Lauren Gardner and EYEBEAM for past lesson plans*

### Support

This program is supported, in part, by public funds from the New York City Department of Cultural Affairs in partnership with the City Council. And by Babycastles members. Thank you.
