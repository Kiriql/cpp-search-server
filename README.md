# SearchServer

## Educational project of the Yandex Workshop course "C++ Developer"
SearchServer is a system for searching documents using keywords.

Main functions:

- ranking search results according to the TF-IDF statistical measure;
- processing of stop words (they are not taken into account by the search engine and do not affect search results);
- processing negative keywords (documents containing negative keywords will not be included in search results);
- creation and processing of a request queue;
- removal of duplicate documents;
- pagination of search results;
- ability to work in multi-threaded mode;

## Principle of operation
Creating an instance of the SearchServer class. A string with stop words separated by spaces is passed to the constructor. Instead of a string, you can pass an arbitrary container (with sequential access to elements and the ability to use it in a for-range loop)

The AddDocument method adds documents for search. The document id, status, rating, and the document itself in string format are passed to the method.

The FindTopDocuments method returns a vector of documents according to the matches of the passed keywords. The results are sorted by the TF-IDF statistical measure. Additional filtering of documents by id, status and rating is possible. The method is implemented in both single-threaded and multi-threaded versions.

The RequestQueue class implements a queue of requests to a search server that stores search results.

## Assembly and installation
Build using any IDE or build from the command line

## System requirements
C++ compiler supporting C++17 standard or later
