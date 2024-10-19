# Hangman Game With Advanced Guessing Strategies

This project implements a Hangman game with multiple [NLP](https://en.wikipedia.org/wiki/Natural_language_processing)-based guessing algorithms. It allows for evaluating the performance of various guessing strategies using the Brown corpus as the source of words.

## Guessing Strategies

The project includes several guessing strategies that vary in complexity:

- `random_guesser`: selects a random letter from the alphabet that hasn't been guessed yet
- `unigram_guesser`: selects a letter based on their frequency in a training set of words
- `unigram_length_guesser`: select a letter based on frequency for words of the same length
- `bigram_guesser`: select a letter based on the letter that precedes it in the word
- `advanced_guesser`: selects a letter considering bidirectional bigrams and trigrams

## Performance

The table below shows the average number of incorrect guesses for each guesser during testing:

| Guesser                  | Average mistakes |
| ------------------------ | ---------------- |
| `random_guesser`         | 16.5             |
| `unigram_guesser`        | 10.2             |
| `unigram_length_guesser` | 10.17            |
| `bigram_guesser`         | 8.74             |
| `advanced_guesser`       | 7.34             |

## Usage

It is recommended to run the code for this project within a development container in VS Code.

```sh
git clone https://github.com/wille-wang/hangman.git
cd hangman
code .
devcontainer open .  # Install `ms-vscode-remote.remote-containers` in VS Code first
```
