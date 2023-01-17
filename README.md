# HarryPotter_Vs_GameOfThrones_Part_2
### Overview
This is a continuation of part 1. The goal of this project was to gather two texts and do a comparison using Part-of-Speech tags and phrases containing particular tags.  The Two texts chosen were both fantasy books, and both first in a series.  One is Harry Potter with the target audience being adolescence and the other is Game of Thrones (book 1) targeted at adults.  Both books were obtained from kaggle.  The goal is to find differences in POS tags in books targeted towards adolescence vs. adults and to look at the difference in top words of each tag type and phrase type.
### Cleaning
Extensive cleaning needed to be done this included removing page numbers, book titles and author names from each page.  There was many typos and errors when the books were brought into the Kaggle database.  This cleaning was accomplished with Regular expressions.
### Vectorization and POS Tagging
Since we needed to add POS tags vectorization needed to be done in a specific way. Each senctence was tokenized and then each word in each sentence was tokenized.  This left us with a list of list of tokens and each token was then tagged with its POS.  This gives us a tupple and the tupples are added to a list that is contained in another list so that the structure of the book is kept the same(words in a each sentence in the same order and sentences in the book in the same order). AN example of output is shown below

![image](https://user-images.githubusercontent.com/118774600/213005637-b4d07365-94e3-416c-9034-47526d9e2fa1.png)

### Percentage of POS tags
A count for each POS tage was found and divided by the total number of words in the book.  This was graphed to show the distrubution of POS tags. (Shown below)

![image](https://user-images.githubusercontent.com/118774600/213006023-92719138-f0e9-4865-ae02-927bf23b541b.png)

![image](https://user-images.githubusercontent.com/118774600/213006067-11de3ed0-9d02-4ad1-9d46-f3af797063f5.png)

### Top Phrases
Using a regular expressions to isolate the POS tags where two tags are in a row. The first tag will consist of either RB (Adverb), RBR (adverb comparative), or RBS (adverb superlative) followed by JJ (adjective), JJR (adjective comparative), JJS (adjective superlative). These two tokens together are an “adjective phrase”. Using the adjective phrases the frequency was found and the top 50 most common are displayed. Lastly it shows how many sentences of the entire book contain an adjective phrase.  This was done for Adjective phrases, Adverb Phrase, and Determiner Noun phrases.  An example output is shown below.

Game of Thrones

![image](https://user-images.githubusercontent.com/118774600/213012200-e60164a4-b3aa-4488-ace7-0df761611f3f.png)

Harry Potter

![image](https://user-images.githubusercontent.com/118774600/213012345-99cddbd8-9584-4ce7-a135-9d190aed0476.png)

###Sentence Length Comparison containing differenct types of phrases
Sentences containing each phrase type were parsed out then the number of tokens in each sentence was obtained from the list of lists of tuples and the sum of the number of tokens was dived by the number of sentences to obtain an average number tokens in each sentence for sentences containing that pharse type.  The results were then graphed and that is shown below.

![image](https://user-images.githubusercontent.com/118774600/213013058-11a8c422-e6a2-4e51-a4b7-130e2bb819c0.png)

###Top 10 word type frequncy distribution comparison
The top words of the POS types adjectives, adverbs, nouns, and verbs were obtained and the top 10 of each was shown in a graph one for each book this is shown below.

![image](https://user-images.githubusercontent.com/118774600/213013384-da681c19-31f4-489f-9aca-590e675ba757.png)

![image](https://user-images.githubusercontent.com/118774600/213013422-4272c3e4-38b7-48ac-8911-1f0850bd6dd5.png)

###Sentiment Recommendations
There is a short section on Possible ways to use POS tagging for sentiment analysis.
