# bleu_score

Closely-related Languages Competition

ntroduction: This challenge involves a simplified machine translation problem, effectively between two writing systems of the same language. We will again be looking at the Irish language, which was the subject of the initial mutation challenge as well. In the 1940's and 1950's, the spelling and grammar of the language were greatly simplified, and the resulting system is the one still in wide use today. One down side, though, is that NLP systems trained on the modern language are not as effective on texts published before the reform, and even simple tasks like searching databases of older texts can be challenging. One solution to this problem is to develop a system for modernizing older texts, which can be thought of as a machine translation problem between two very closely-related languages! In fact, we even have a reasonably large amount of parallel text which we can use for training such a system, in the form of old books that have been manually updated to the new spelling and grammar for modern readers.

Training/Test Set: The training data for this challenge is taken from just such a parallel corpus of manually modernized texts. I chose twenty books and restricted to authors from the same (Ulster) dialect area. The full training corpus consists of about 47,000 parallel sentences, nearly one million words of text on both the source and target side. The test corpus consists of 1000 parallel sentences, with about 25,000 words on each side.

The training data is provided in two separate files named train-source.txt and train-target.txt. The source and target texts were tokenized and both files contain one token per line. The special token <s> marks the beginning of a sentence, and </s> marks the end of a sentence (the sentences are aligned one-to-one, so you'll find the same number of sentences in each file). If you need development data in order to tune the parameters of your model(s), you'll need to take a subset of the training data for that.

*** Download Training Data (3MB)

Download Download Training Data (3MB)

*** Download Test Data (80K)

Download Download Test Data (80K)

Evaluation: The goal is to train a system that achieves the highest possible BLEU score

Links to an external site. on the test set.

Deliverables and Grading: You will implement two solutions to the given challenge; one “from scratch” implementation that doesn't use any NLP or machine learning libraries, and one “anything goes” implementation in which you're free to use additional libraries, code, or (particularly useful in this case) linguistic knowledge. It's unlikely you would be able to find or produce additional training data, but even if you do, I'll ask you to only use the provided parallel texts for training. Details regarding the format of your submission and the grading scheme are provided in the Rubric for NLP Challenges document.

For this particular challenge, the code you submit should read the training data files train-source.txt and train-target.txt from the same directory it's launched from. There is a sample notebook

Links to an external site. in the course github repo that you can use to begin your work (of course you won't be able to do the final evaluation without access to the test files, but you can (and should!) track your progress by setting aside a development set). You are free to restructure your code however you'd like, but I'd like the last line to call the “evaluate” function which displays the BLEU score of your two algorithms on the test set.

How to submit: The best way to submit your code is by committing it to a git repository (on github or on the CS Department gitlab instance for example) that I'd be able to clone within my hopper account.