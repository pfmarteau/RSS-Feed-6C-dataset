# RSS-Feed-6C-dataset
Dataset for text classification: items belong to 6 categories

This dataset contains french and english textual documents collected on the following rss sources during November 2018 :

## English sources


## French sources
1. http://www.sports.fr/fr/cmc/rss.xml SPORT
2. https://rmcsport.bfmtv.com/rss/info/flux-rss/flux-toutes-les-actualites/ SPORT
3. https://www.santepubliquefrance.fr/content/view/rss/426 SANTE_MEDECINE
4. http://www.sfmg.org/rss/actualites_2-4-5-10-14-18.xml SANTE_MEDECINE
5. https://www.futura-sciences.com/rss/actualites.xml SCIENCE
6. http://le-fil-science.cea.fr/actualites-scientifiques/_layouts/15/i2i/web/ceasrchrss.ashx?pid=9&wid=g_28aebe78_981c_4b25_8436_c0bef19229fa SCIENCE
7. http://www.lefigaro.fr/rss/figaro_politique.xml POLITIQUE
8. https://www.lemonde.fr/politique/rss_full.xml POLITIQUE
9. https://syndication.lesechos.fr/rss/rss_france.xml ECONOMIE
10. https://bfmbusiness.bfmtv.com/rss/info/flux-rss/flux-toutes-les-actualites/ ECONOMIE
11. http://www.culture.gouv.fr/rss/feed/actualites ART_CULTURE
12. http://www.culture.be/index.php?id=5146&type=100 ART_CULTURE

## Organization of the data
The dataset comes with two xml files, one for each language. 

Each rss item is structured as follows:
```
<item>
  <title> MP yyyy to face retrial in speed ticket case   </title>
  <description> Peterborough MP XXX denies a charge of perverting the course of justice  </description>
  <text> A Labour MP accused of lying about who was driving her speeding car will face a retrial after a jury failed to 
         reach a verdict ...  </text>
  <tag> POLITIQUE</tag>
</item>
```

Hence, the classification can be performed using the concatenation of all textual fields, namely <title> + <description> + <text>. SOme of these fields may be missing.
  
The <tag> field gives the category that belongs to one of the six categories ['ART_CULTURE', 'ECONOMIE/ECONOMY', 'POLITIQUE/POLITICS', 'SANTE_MEDECINE/HEALTH_MEDICINE', 'SCIENCE', 'SPORT'].
