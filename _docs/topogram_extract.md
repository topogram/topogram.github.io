---
layout: docs
title: Define topogram
step: 8
---

To create a topogram, you will be presented with  different options :

*  **add stopwords** : the words listed here will be ignored during the processing (for instance, you could ignore APEC as it is redondant in every message you have here)
* **maximum words / citations** :  this will determine the maximum number of words or citations to display
* **citations & patterns** : here you can input specific patterns to match in the text and create graphs from those patterns. For instance, user citations in Sina Weibo or Twitter (@什么人) is already added by default. You just have to select " @ weibo" in the list to extract all user mentions in the dataset.

![extract topograms](/uploads/topogram_extract.png)

NB : You can add also patterns yourself :  The input should be done in the "Add Patterns" field using "regular expressions" (see inline help on this). You can browse the results by looking at the sample (next / prev buttons), the click on **Add Pattern**. Once the pattern is setup, you can click on the "Create Topogram" button.
