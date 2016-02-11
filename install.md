---
layout: page
title: Install Topogram
---

Tested on Debian Jessie.

### Topogram


    pip install topogram

### Topogram API

Python, Mongo and Redis are required.

    git clone http://github.com/topogram/topogram-server
    cd topogram-server
    pip install -r requirements.txt
    rqworker taf # run the data worker
    python run.py # run the web server



### Topogram Client

Meteor is required - can be installed with ```npm -g install meteor```

    git clone http://github.com/topogram/topogram-client
    cd topogram-client
    meteor
