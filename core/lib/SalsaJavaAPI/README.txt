This folder contains a Java API to process the SALSA XML corpora. 

Browse the Javadoc in the 'doc' folder for more information, and start reading with the 'salsa.corpora.elements.Corpus' class. 


The API consists of elements that represent a SALSA XML file. 

----
To read in a Corpus from a file, write the following lines into your source code: 

CorpusParser parser = new CorpusParser();

Corpus corpus = parser.parseCorpusFromFile("corpusIWantToRead.xml");

-----

----
To write out the XML representation of a given Corpus data structure into a file, write: 

MyFileWriter fileWriter = new MyFileWriter("newCorpusName.xml");

fileWriter.writeToFile(corpus.toString());
--------


-------
When you have a Corpus data structure, you can navigate through the Corpus just like navigating through the XML file. For example, to get a list of all sentences in the corpus, you write: 

Body body = corpus.getBody();

ArrayList<Sentence> allSentences = body.getSentences();
---------


In this way, you can do anything you want with the SalsaXML corpora. Just always follow the 3 steps: 

- read in a corpus from a file
- do something with the corpus
- write out the corpus to another file, using the Corpus.toString() method.













@created by fabians 28-08-2009
