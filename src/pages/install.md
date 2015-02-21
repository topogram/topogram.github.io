---
template: page.html
title: Install Topogram
---

### Requirements 

Topogram have been tested on Debian Wheezy. You can use the install script (Internet connection required).

    bash install.sh

#### Step by step

Install python, git and pip

    apt-get update
    apt-get install build-essential git git-core python-dev python-setuptools python-pip

Install python dependencies

    pip install -r requirements.txt
    pip install fabric fabric-virtualenv

Install elasticsearch

    wget https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-1.3.2.deb
    dpkg -i elasticsearch-1.3.2.deb

Install node

    apt-get install node

Install frontend dependencies (bower required)

    npm install -g bower
    bower install

Get started !

    python run.py

### How to install

    git clone http://github.com/topogram/topogram-server
    cd topogram-server
    pip install -r requirements.txt
    python run.py
