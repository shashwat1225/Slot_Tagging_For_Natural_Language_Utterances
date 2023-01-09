# Slot Tagging for Natural Language Utterances
This repository contains code for a project that aims to tag slots in natural language utterances. The tags indicate the entity or concept mentioned in the utterance. For example, in the utterance "list the cast of the movie the campaign", the slots would be "movie" and "cast".

## Getting Started
To get started, you will need to install the following dependencies:

* Pandas
* NumPy
* PyTorch
* Scikit-learn
You can install these dependencies using `pip`.

Once you have installed the dependencies, you can use the provided code to train and test a model for slot tagging on the provided dataset.

## Dataset

The dataset used for this project is provided in the form of two CSV files: `hw2_train_20221024.csv` and `hw2_test.csv`. The training set is used to train and validate the model, while the test set is used to evaluate the model.

The dataset consists of natural language utterances and their corresponding slot tags. The slot tags are in the IOB (Inside, Outside, Beginning) format, where each word in the utterance is tagged as either `I` (inside), `O` (outside) or `B` (beginning) depending on whether it is part of a slot or not. For example, in the utterance "list the cast of the movie the campaign", the tags would be `O O O O O B_subject I_subject I_subject O`.

## Preprocessing

The provided code performs preprocessing on the dataset to prepare it for training and evaluation. This includes:

* Creating vocabulary and tag lists from the utterances and tags in the dataset
* Assigning unique identifiers to each word and tag in the vocabulary and tag lists
* Vectorizing the utterances and tags by replacing each word and tag with its corresponding unique identifier
* Padding the vectorized utterances and tags to a uniform length

## Model Training and Evaluation

A model is trained using the vectorized training set, and its performance is evaluated on the vectorized validation set. The model consists of an embedding layer, two LSTM layers and a linear layer. It is trained using the Adam optimizer and the cross-entropy loss.

The model's performance is measured using the F1 score and the accuracy. The training and validation scores are plotted to visualize the progress of training.

Once the model is trained, it is evaluated on the vectorized test set and the F1 score and accuracy are reported.

## Conclusion
The provided code can be used to train and evaluate a model for slot tagging on the provided dataset. The model can be further fine-tuned and improved by experimenting with different hyperparameters and architectures.
