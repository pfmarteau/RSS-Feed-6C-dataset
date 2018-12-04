# RSS-Feed-6C-dataset
Dataset for text classification: items belong to 6 categories

This dataset contains french and english textual documents collected on the following rss sources during November 2018 :

## English sources


## French sources

## Organization of the data
The dataset comes with two xml files, one for each language. 

Each rss item is structured as follows:
```
<item>
  <title> MP Fiona Onasanya to face retrial in speed ticket case   </title>
  <description> Peterborough MP XXX denies a charge of perverting the course of justice  </description>
  <text> A Labour MP accused of lying about who was driving her speeding car will face a retrial after a jury failed to 
         reach a verdict ...  </text>
  <tag> POLITIQUE</tag>
</item>
```

Hence, the classification can be performed using the concatenation of all textual fields, namely <title> + <description> + <text>. SOme of these fields may be missing.
  
The <tag> field gives the category that belongs to one of the six categories ['ART_CULTURE', 'ECONOMIE', 'POLITIQUE', 'SANTE_MEDECINE', 'SCIENCE', 'SPORT'].
