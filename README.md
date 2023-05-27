# Roman Urdu-poetry-generation-using-generative-modeling


This repository contains a project on Poetry Generation in Roman Urdu using n-gram language modeling. The project utilizes the spaCy pipeline for text processing and aims to generate a ghazal consisting of seven stanzas, each containing two verses.

## Introduction
The task of this project is to generate poetry by training n-gram models on a poetry corpus. The generated poetry will follow the structure of a ghazal, with each stanza consisting of two verses. The length of each verse should be between 6 to 8 words. The poetry corpus can be augmented by scraping online sources to obtain a better representation of Urdu poetry. The models can be trained on either Roman Urdu or Urdu text, with the option to convert the generated version into Roman Urdu using the implementation from Assignment 1.

## Assignment Task
The task involves generating a ghazal using different models. The implementation will generate one verse at a time until all stanzas have been generated. The following algorithm can be used to solve the poetry generation problem:

## Load the Poetry Corpus
Tokenize the corpus to obtain a list of words
Generate n-gram models (bigram and trigram)
For each stanza:
For each verse:
Generate a random number between 6 and 8 (inclusive) to determine the verse length
Select the first word intelligently
Select subsequent words until the end of the verse, using the most probable next word based on the chosen word
[bonus] Attempt to rhyme the last words of the stanza with the last word of the first stanza
Print the verse
Print an empty line after each stanza
Implementation Challenges
The challenges of this assignment include selecting subsequent words intelligently after choosing the first word of the verse. To predict the next word, it is essential to compute the most probable next word among all the possible options. This can be achieved by using a Conditional Frequency Distribution (CFD) that provides the likelihood of each possible outcome given a condition. Additionally, rhyming the generated verses can be a challenge, requiring the construction of a rhyming dictionary.

## Standard n-gram Models
The project utilizes the Conditional Frequency Distribution (CFD) approach to develop both the Bigram model and Trigram model. The first word of each line is randomly selected from the starting words in the vocabulary, and the bigram model is used to generate the next word until the verse is complete. The same steps are followed for the trigram model, and the results of both n-gram models are compared. [bonus] Additionally, the possibility of making the sonnet rhyme is explored by building a pronunciation dictionary using the most probable rhyming endings.

## Backward Bigram Model
In some cases, words may be better predicted from their right context rather than their left context. To address this, a Backward Bigram model is implemented, which models the generation of a sentence from right to left. The Backward Bigram model is created by modifying the Bigram model to change the modeling direction. The results of the backward bigram model are compared with previous implementations.

## Bidirectional Bigram Model
The Bidirectional Bigram model combines the forward and backward models to generate output. Both the Backward Bigram model and Bidirectional Bigram model take the same input and produce the same style of output as the Bigram model. The output of the Bidirectional Bigram model is compared with the Trigram model.

## Usage
Clone the repository:


Install the required dependencies mentioned in the project documentation.

Prepare the poetry corpus: This can involve collecting existing poetry datasets and scraping online sources for additional data.

Tokenize the corpus: Use the provided scripts or modules to tokenize the corpus and obtain a list of words.

Generate n-gram models: Implement the algorithms for generating the Bigram and Trigram models using the tokenized corpus.

Run the project: Execute the main script or launch the application to generate the ghazal.

Explore the generated poetry: The project will print the ghazal, consisting of seven stanzas with two verses each, following the specified constraints.

### Customize and enhance:
Modify the codebase to experiment with different models, incorporate additional datasets, or improve the poetry generation algorithms as desired.
