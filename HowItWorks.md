---
layout: page
title: How it Works
---

Topogram is a web-based and open-source toolkit to extract and visualize social, semantic and spatio-temporal dynamics within large sets of data. The purpose of this tool is to bring elements of contexts while studying and exploring large sets of text data that describe online activities, understood as online enunciation acts. Topogram link together different dimensions of the data : words (lexical analysis), relationships (networks), time (changes and evolution) and space (geographic mapping).


Topogram is divided into 3 main parts

1. **topogram** : a data mining library to extract networks of words, citations and places from raw data
2. **topogram-api** : a webserver providing a REST API to access the library
3. **topogram-client** : a collaborative visualization interface to edit, annotate and publish graphs


## Topogram

---

**[Topogram](https://github.com/topogram/topogram)** is a data mining library.

It won’t take care of the visualization but it will clean and format your data sets, so you can directly plug the output into something like d3js or matplotlib to see nice colored things.

Topogram relies on three core components :

* *corpora* : files or stream from CSV, Mongo, Elastic Search, etc.
* *processors* : dates formatters, NLP parsers, relationships extractors, etc.
* *viz parsers* : data containers returning clean and ready-to-use data for a visualization (time series, network graph, map, etc.).


{% highlight python %}

# Extract a network of words from a dataset

from topogram.corpora import CSVCorpus
from topogram.processors import CSVCorpus
from topogram.viz_parsers import WordsNetwork

corpus = CSVCorpus("your_data.csv")
nlp = NLP("english")
words_network = WordsNetwork(directed=False)

for row in corpus:
    words = nlp(row["content"])
    words_network(words)

print words_network.to_JSON() # return a dict with weighted edges and nodes

{% endhighlight %}

View [Topogram on Github](https://github.com/topogram/topogram)

## Topogram API

**Topogram API**

View [Topogram API on Github](https://github.com/topogram/topogram-server)

{% highlight bash %}

  # logging in
  wget --save-cookies cookies.txt \
    --post-data 'email=my@email.com&password=mypassword' \
    http://localhost:5000/api/v1/sessions

  # gettings a list of all existing datasets
  wget --load-cookies cookies.txt \
    -p http://localhost:5000/api/v1/datasets

{% endhighlight  %}

## Topogram Client

**Topogram Client** is a web-based network visualization interface allow to browse networks, based on words, places and times.

Data can be browsed through any of those different dimensions : selection of a specific timeframe or geographic zone, lookup of specific words and terms, selection of  parts of the graph, etc.
