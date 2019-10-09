# Smooshed Morse Code

Morse code is a character encoding scheme that encodes text characters as standardized sequences of dots and dashes. It was created by Samuel Morse, the inventor of the telegraph.

For the purpose of this challenge, Morse code represents every letter as a sequence of 1-4 characters, each of which is either . (dot) or - (dash). Normally, you would indicate where one letter ends and the next begins with a space between the letters' codes. For example, the code for SOS would be represented as follows:

```
... --- ...
```

For this challenge, however, the spaces will be removed, so instead the morse code would read

```
...---...
```

## The Challenge (Basic)

Allow a user to enter a word into the program. Translate that word to Morse code, and then translate that to Smooshed Morse code. Given a word in Smooshed Morse code, translate that code back to your original word.

### Examples
```
sos: ...---...
daily: -...-...-..-.--
programmer: .--..-.-----..-..-----..-.
bits: -.....-...
three: -.....-...
```

An obvious problem with this system is that decoding is ambiguous. For instance, both bits and three encode to the same string, so you can't tell which one you would decode to without more information. If there is more than one option, make sure to list all possibilities. Check your words against the [enable1 word list](https://raw.githubusercontent.com/dolph/dictionary/master/enable1.txt), which contains 172,823 words.

### Bonus

See if you can figure out the words in these challenges:

1. The sequence -...-....-.--. is the code for four different words (needing, nervate, niding, tiling). Find the only sequence that's the code for 13 different words.
2. autotomous encodes to .-..--------------..-..., which has 14 dashes in a row. Find the only word that has 15 dashes in a row.
3. Call a word perfectly balanced if its code has the same number of dots as dashes. counterdemonstrations is one of two 21-letter words that's perfectly balanced. Find the other one.
4. protectorate is 12 letters long and encodes to .--..-.----.-.-.----.-..--., which is a palindrome (i.e. the string is the same when reversed). Find the only 13-letter word that encodes to a palindrome.
5. --.---.---.-- is one of five 13-character sequences that does not appear in the encoding of any word. Find the other four.

## Stretch (Intermediate)

A permutation of the alphabet is a 26-character string in which each of the letters a through z appears once.

Given a smooshed Morse code encoding of a permutation of the alphabet, find the permutation it encodes, or any other permutation that produces the same encoding (in general there will be more than one). It's not enough to write a program that will eventually finish after a very long period of time: run your code through to completion for at least one example.

### Examples
```
.--...-.-.-.....-.--........----.-.-..---.---.--.--.-.-....-..-...-.---..--.----..
  => "wirnbfzehatqlojpgcvusyxkmd"
.----...---.-....--.-........-----....--.-..-.-..--.--...--..-.---.--..-.-...--..-
  => "wzjlepdsvothqfxkbgrmyicuna"
..-...-..-....--.---.---.---..-..--....-.....-..-.--.-.-.--.-..--.--..--.----..-..
  => "uvfsqmjazxthbidyrkcwegponl"
```

Again, there's more than one valid output for these inputs. [Here's a list of 1000 inputs](https://gist.github.com/cosmologicon/415be8987a24a3abd07ba1dddc3cf389#file-smorse2-bonus1-in). How fast can you find the output for all of them? A good time depends on your language of choice and setup, so there's no specific time to aim for.

### Bonus

Typically, a valid input will have thousands of possible outputs. The object of this bonus challenge is to find a valid input with as few possible outputs as possible, while still having at least 1. The following encoded string has 41 decodings:

```
......-..--...---.-....---...--....--.-..---.....---.-.---..---.-....--.-.---.-.--
```

Can you do better?

## Stretch (Hard)

Decode smooshed Morse code representations of English text. The decoding is ambiguous. You're not expected to do a perfect job, but the more your output resembles English, the better you're doing. You are not expected to reproduce the punctuation, just the spacing between words.

A standard approach involves training on a corpus of English text. You can use any training data sources you want, but your program must run autonomously on the input, without human intervention.

The challenge inputs this time are all English-language movie quotes, some of which involve proper names, contractions (without the apostrophe), or other words you might not find in a standard word list.

### Example

Input

```
-.---..--.....--.--..-..-.--....--.--..-.--.-.....--.-......-....-......-...-.-......-.--.--.--
```

Output

```
no im simply saying that life uh finds a way
```

Try your hand at these:

Input 1

```
......---.--..--...-....-..-----.....-..-.--.-.-.-..-.--.-....-.-.-.....--..-..-...-.--.-...--..--.----.-.--..--...-.-.-.....--.--.....----.-.....-.-..----..-.-.-..-....--...-........-.---.-.....-..-.-.-.---.--.--...-....-...----....----.---.-..-..--...-...-..-.-.-..----.
```

Input 2 (contains proper names)

```
...--.--.-----.......---.---.-----..-...-----.-......-.--.....----.--.-.-..-..---......-...--.-...-..-------.--.-..-..---.....-...-....-....-.-...-.-.....-.--.---...-..-.-.--.-.-....--..-.-....-.--..--....-.---.....-...-..-..----...--.....-.-.-----..--.-..--......-...-.-.-----.---.--..-.-..-......--..-...-.-..----..-..-.---.........----..-.-..--.-....-.-..--.-....-.-..-..--.-.----.-.-.---.-...-...-..-...-.--.---..-...-.-..--....-.....-...-..--...-.---......---.-.--..--...........--...-.-.----.-.-..--.-.----.-.....--....---.-.-.....---.....-.--..--..-.-----.....-..-.-..-.-.-..-.--.--.-.--.-..-...-..-...--....---.-...-..-.-----.---..-.......--........-.....-.-.......---..-......--..-...-...-.-....-...-.-.......
```

Input 3

```
-.-----..-.-..-......-.......-..........------..-..-.-..--.-..-.-....-.---..-..--...--.-....-.-...--.-.
```

## Resources

This challenge was originally posted to Reddit by [u/Separate_Memory/](https://www.reddit.com/u/Separate_Memory/). It was posted to the [r/dailyprogrammer/](https://www.reddit.com/r/dailyprogrammer/) subreddit.

* [Morse Code - Wiki](https://en.wikipedia.org/wiki/Morse_code)
* [Challenge #380 (Easy) Smooshed Morse Code](https://www.reddit.com/r/dailyprogrammer/comments/cmd1hb/20190805_challenge_380_easy_smooshed_morse_code_1/)
* [Challenge #380 (Intermediate) Smooshed Morse Code](https://www.reddit.com/r/dailyprogrammer/comments/cn6gz5/20190807_challenge_380_intermediate_smooshed/)
* [Challenge #380 (Hard) Smooshed Morse Code](https://www.reddit.com/r/dailyprogrammer/comments/co5i4t/20190809_challenge_380_hard_smooshed_morse_code_3/)
