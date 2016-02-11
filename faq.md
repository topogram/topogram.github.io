---
layout: page
title: FAQ
---


## General questions

---
*You will find here answers to commonly ask questions about Topogram*

#### What is Topogram ?
*Topogram* is an open-source web toolkit to map social, semantic and spatio-temporal dynamics.


#### Why Topogram ?
It answers the growing need for interactive mapping of complex online and offline interactions. Also because you need to be able to make sense of a bunch of text data without hours of development. Finally, because you may want to own your research environment and still be able to use it in your web browser so you can share results and analysis process easily.

#### How does it work ?
See the [How It Works](/HowItWorks) section.

#### How can I start to use Topogram ?
* Download and install Topogram on your own computer by following the [Install instructions](/install).
* If you need to deploy it on a web server, just use the scripts at [topogram-deploy](https://github.com/topogram/topogram-deploy). The instructions are in the README file.
* Topogram is also available as an online service on [app.topogram.io](https://app.topogram.io).

#### Which technology does Topogram use ?
* All data analysis (crunch numbers, NLP, etc.) are made with [Python](http://python.org)
* The web server is made with Python [Flask](http://flask.readthedocs.org) for the API, and use Redis for workers and Mongo for data storage. A mySQL/SQLite db is used to store user-related  informations (emails, passwords, contents, etc.)
* The client is made with Meteor JS and use [d3.js](http://d3js.org), [Leaflet](http://leaflet.org) and [Cytoscape](http://js.cytoscape.org) to draw visualizations, networks and maps.


#### Where does Topogram come from ?
*Topogram* is evolved from the phD research of [Clément Renaud](http://clementrenaud.com) about Internet memes on the Chinese social network Sina Weibo. You can read the [thesis](clementrenaud.com/uploads/phD/thesis.pdf) for more background on the project.

#### How can I quote Topogram in my paper ?
For now, you can quote this conference paper using this [Bibtex entry](/uploads/topogram.bib)

    Renaud, C. (2014). Meme observation and classification on a large corpus of tweets from Sina Weibo Memes on Sina Weibo. In *Chinese Internet Research Conference (CIRC14)* (pp. 1–9). HK.

#### How can I get in touch with you and/or contribute to Topogram ?

* Drop us an email at [hi@topogram.io](mailto:hi@topogram.io)
* Open an issue on [Github](http://topogram/topogram)
* Join the conversation on [Slack](http://topogram.slack.com)

Talk to you soon !
