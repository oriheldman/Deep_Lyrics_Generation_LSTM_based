# Lyrics Generation - Using Deep Learning

## Overview
In this project we trained a neural network to generate lyrics to a song based on the provided
melody. We experiment and analyze 2 different architectures trained for this task.
During the training phase of the model, both the lyrics of a song and its melody are available.
The melodies are stored in .mid (MIDI files) and contain various types of information except
the lyrics. We incorporate the midis information with the lyrics. During the test phase, we
automatically generate lyrics for a provided melody and a single seed word.

## Data
The dataset used for training and testing the NN for this task is composed of the song's lyrics
and its matching melody provided in a midi file format. The data contains songs from various
artists, genres and centuries. For each instance in the dataset, the artist, song name, and
the lyrics are provided. The ‘&’ character in the lyrics states the end of a sentence.

## DNN Architecture (LSTM based)
The model takes as an input a sequence of words and passes their word embeddings to an
LSTM. The output of the last hidden uint of the LSTM is concatenated with the midi vector of
the current sequence. This vector is passed to a FC layey for combining the meanings of the
lyrics with the midi features. Then, another FC layer whose length is the vocabulary size,
followed by a softmax function to compute the distribution over the vocabulary.

## Generated Lyrics Examples (sample)
### Melody: "Aqua - Barbie Girl", First seed word: "baby"
baby can i make you feel chaka

let me superman for you

da get tragic but to change or bitin

turn a young clothes went

could i make you got crying with like i

despise

take you

with me for this will it

but because nothing

lido ah and if you been so mean

just in the poison as a mind on my greatest

your name just whoawhoawhoawhoa

a oohoohoooooo tonight in a guy from your

biggest....
