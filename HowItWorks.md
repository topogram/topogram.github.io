---
layout: page
title: How it Works
---

[Topogram](https://github.com/topogram/topogram) is a collaborative interface to visualize, edit, annotate and publish graphs online.

![](/images/Topogram-Network.png)

### Data
---

You can create networks by:

* importing CSV files containing nodes and edges from the interface
* using the [Python API Client](https://github.com/topogram/topogram-api-client) to push data from a script
* adding nodes and edges manually from the interface

You can use different options such as *color* or *weight* but also *longitude* / *latitude* for geo coordinates and *start* and *end* for time information (*start* only for a time point).

<div class="row">

<div class="four columns" markdown="1">

| node | color | size |
|---|---|---|
|a|blue|5|
|b|red|10|
|c|green|5|

*Node Data*

</div>
<div class="four columns" markdown="1">


| source | destination | weight |
|---|---|---|
|a|b|1|
|b|c|1|
|c|a|5|

*Edge Data*
</div>
<div class="four columns" markdown="1">

  {% include network.html nodeData=1 id="networkNodes" %}
</div>
</div>


### Annotations
---

<div class="row">

<div class="four columns" markdown="1">

#### Real-time annotations

You can annotate and comment in the graph in real-time with other people

</div>

<div class="seven columns">

  {% include form.html %}
</div>
</div>
