---
layout: page
title: How it Works
---

Topogram relies on 2 main components

1. [Topogram]( https://github.com/topogram/topogram ) : a Python library to extract networks from raw data
3. [Topogram Client](https://github.com/topogram/topogram-client) : a collaborative interface to visualize, edit, annotate and publish graphs

The communication between the both can assured by a [redis](http://redis.io/) worker and
a data store, like [Elastic Search](https://www.elastic.co) for instance.


## Import Data

The data you provide to Topogram should follow this format :

| name | description | format | example|
|---|---|---|---|
**text** | some text that you want to analyze | [UTF-8](https://en.wikipedia.org/wiki/UTF-8) | *Hello, how are you @topogram ?*
**timestamp** | a well-formatted time indication | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) | *2016-02-12T03:21:55+00:00*
**source** | The origin of the message | [UTF-8](https://en.wikipedia.org/wiki/UTF-8) | *@clemsos*
**destination** | the field of destination | [UTF-8](https://en.wikipedia.org/wiki/UTF-8) | *@topogram*
**additional info** | other relevant informations | [JSON](https://en.wikipedia.org/wiki/JSON) | *{'mobile' : 'iphone', 'retweets' : 1}*


NB: Some [utils](http://topogram.readthedocs.org) are in available to convert CSV files and data streams from Mongo or Elastic Search in this format.

## Extract networks

the [Topogram](http://github.com/topogram/topogram) Python library can extract networks of words, citations and places. It can be used from [command-line](http://topogram.readthedocs.org/en/latest/cli.html) or in a Python script. It relies on 3 components :

* corpora : parse a corpus in CSV or stream directly from Mongo, Elastic Search, etc.
* processors : basic tools to format dates, extract relationships, etc.
* viz parsers : data containers that will return clean and ready-to-use data for a visualization (time series, network graph, map, etc.).

{% highlight python %}

# Extract a network of words from a dataset

corpus = CSVCorpus(your_data.csv )
nlp = NLP("english")
words_network = Network(directed=False)

for row in corpus:
    words = nlp(row["content"])
    words_network(words)

print words_network.to_JSON() # return a dict with weighted edges and nodes

{% endhighlight %}

You can use custom processors - see this example with [Elastic Search](). For more, read [the docs](http://topogram.readthedocs.org) or view on [ Github](https://github.com/topogram/topogram).

## Visualize, correct and publish

[Topogram Client](https://github.com/topogram/topogram-client) is a web-based network visualization interface to browse, edit and publish networks.

---

<div class="row">

<div class="four columns" markdown="1">

#### Edge data

To start, you should import some [network data](https://en.wikipedia.org/wiki/Network_model). You can import the data generated with [Topogram](https://github.com/topogram/topogram) or your own set of edges, following this basic model.

</div>
<div class="four columns" markdown="1">

| source | destination | weight |
|---|---|---|
|a|b|1|
|b|c|1|
|c|a|5|

</div>
<div class="four columns">
  {% include network.html nodeData=0 id="networkBasic" %}
</div>
</div>

---

<div class="row">
<div class="four columns" markdown="1">

#### Node data

To start, you should import some [network data](https://en.wikipedia.org/wiki/Network_model). You can import the data generated with [Topogram](https://github.com/topogram/topogram) or your own set of edges, following this basic model.

</div>
<div class="four columns" markdown="1">

| node | color | size |
|---|---|---|
|a|blue|5|
|b|red|10|
|c|green|5|

</div>
<div class="four columns">
  {% include network.html nodeData=1 id="networkNodes" %}
</div>
</div>

---

<div class="row">

<div class="four columns" markdown="1">

#### Real-time annotations

You can annotate and comments in the graph in real-time with other people

</div>

<div class="seven columns">

  {% include form.html %}
</div>
</div>
