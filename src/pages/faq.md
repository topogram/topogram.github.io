---
template: page.html
title: Frequently Asked Questions
---

You will find here answers to commnly ask questions about Topogram 

### General questions
___

#### What is Topogram ?
*Topogram* is a web-based dashboard for visualization of data as networks. It allows to easily build dynamic visualization of words, users and places relationships quoted in large corpora of texts by using full-text search.


#### Why Topogram ?
Because you need to be able to make sense of a bunch of text data without hours of development. Also because you may want to own your research environment and still be able to use it in your web browser so you can share results and analysis process easily. 

#### How does it work ?
*Topogram* brings together existing algorithms and technology in a single toolkit. The core technology is located in a [Python library](https://github.com/topogram/topogram) that takes care of the formatting and processing of the data inputs and outputs. Then, a [web application](https://github.com/topogram/topogram-server) allows you to upload data sets, search specific words and phrases in it and visualize different metrics and dynamics for each result. 

#### How can I start to use Topogram ?
* You can download and install Topogram on your own computer by following the [Install instructions](/pages/install).
* If you need to deploy it on a web server, just use the scripts at [topogram-deploy](https://github.com/topogram/topogram-deploy). The instructions are in the README file.
* Topogram is also available as an online service on [app.topogram.io](http://app.topogram.io). Please request an invitation at [hi@topogram.io](mailto:hi@topogram.io) to start use it.

#### Which technology does Topogram use ?
* On the server side, Topogram use [Python](http://python.org) for the Natural Language Processing (NLP) and analysis with a [Flask](http://flask.readthedocs.org) app to serve the final data through a web/REST API. 
* The data is stored in [Elasticsearch](http://elasticsearch.org). A mySQL/SQLite db is used to store user-related  informations (emails, passwords, contents, etc.)
* On the client side, the web app use [AngularJS](http://angularjs.org) to handle data and pages and [d3.js](http://d3js.org)


#### Where does Topogram come from ?
*Topogram* is evolved from the phD research of [Clément Renaud](http://clementrenaud.com) about data mining of social network. You can read the [complete thesis](clementrenaud.com/uploads/phD/thesis.pdf) for more info.

#### How can I quote Topogram in my paper ?
For now, you can quote this conference paper using this [Bibtex entry](/uploads/topogram.bib)

    Renaud, C. (2014). Meme observation and classification on a large corpus of tweets from Sina Weibo Memes on Sina Weibo. In *Chinese Internet Research Conference (CIRC14)* (pp. 1–9). HK.


### Using Topogram
____

#### How can I make my search queries more precise ?

Topogram is using [Elasticsearch parser](http://www.elasticsearch.org/guide/en/elasticsearch/reference/current/query-dsl-query-string-query.html#query-string-syntax) to transform your query into a searchable entity. You can use different operators such as "" (quote marks), AND or OR.

Examples :

* ```lol cat ``` : all posts containing  ```lol``` and ```cat```.
* ```"lol cat"``` : all posts containing the phrase ```lol cat```.
* ``` lol OR CAT``` : all posts containing ```lol``` or ```cat```.
* ``` lol AND CAT``` : all posts containing ```lol``` and ```cat```.

### 
