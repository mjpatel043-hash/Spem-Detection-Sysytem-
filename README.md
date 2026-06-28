#  Spam-Detection-Sysytem-
This is the Cyber security project For Spem Detection System.
<br>
Aurthor -- Meet Patel

Spam Detection System — Summary
## What it is 

A Java console program that checks if a typed message is spam or phishing.
Gives every message a threat score from 0 to 100 percent.

## How a decision gets made

If the score is 75 percent or higher, the message is blocked.
Some messages get blocked instantly, no matter what the score is — explained below.

## Instant block conditions (checked first)

The message contains a known shortened link, such as bit.ly or tinyurl.com.
The message contains a common scam phrase, such as verify-account, claim-now, or free-prizes.
More than half the message is in capital letters, and the message is longer than 10 characters (a common scare-tactic style used in scam texts).

## If none of the above apply

The program uses a method called Naive Bayes to estimate spam probability.
It looks at each word in the message and compares it to words seen before in known spam messages versus known normal messages.
The more "spam-like" words present, the higher the score.

## Before any scoring happens

The text is cleaned up first.
All letters are converted to lowercase.
Common letter-swap tricks are reversed (3 becomes e, 1 becomes i, 0 becomes o).
Unusual punctuation is removed.
This step stops people from sneaking past the filter by misspelling words on purpose.

## Built-in starting data

The program is preloaded with 8 sample messages before you even use it.
4 of these are spam examples, 4 are normal message examples.
This means it can give useful results immediately, without any setup.

## What it's built with
 
Plain Java only — no outside libraries.
No internet connection, no saved files, no database.
Uses Java's built-in HashMap and HashSet to store word counts.
Uses regular expressions to match spam patterns.
Uses basic math (logarithms and exponents) to calculate probabilities accurately.

## Why two methods instead of one

A filter that only checks fixed keywords is easy to trick — attackers just reword things slightly.
A filter that only uses statistics can miss obvious, well-known scams.
Combining both means known attack patterns get caught right away, and newer or reworded spam still has a chance of being caught by the learned model.

## How to run it

Compile: javac SecuritySpamDetector.java
Run: java SecuritySpamDetector
Type any message and press enter to see its score and result.
Type exit to close the program.
