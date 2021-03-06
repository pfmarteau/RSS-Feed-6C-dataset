# RSS-Feed-6C-dataset
Dataset for text classification: items belong to 6 categories

This dataset contains french and english textual documents collected on the following rss sources during November 2018. Please note that each of these source holds a coyright on these collected items.

## English sources
1. http://feeds.bbci.co.uk/sport/rss.xml?edition=uk SPORT
2. http://rss.cnn.com/rss/edition_sport.rss SPORT
3. https://rss.medicalnewstoday.com/featurednews.xml SANTE_MEDECINE
4. https://medlineplus.gov/groupfeeds/new.xml SANTE_MEDECINE
5. http://feeds.bbci.co.uk/news/science_and_environment/rss.xml?edition=uk SCIENCE
6. http://feeds.reuters.com/reuters/scienceNews SCIENCE
7. http://feeds.reuters.com/Reuters/PoliticsNews POLITIQUE
8. http://feeds.bbci.co.uk/news/politics/rss.xml POLITIQUE
9. http://feeds.reuters.com/reuters/businessNews ECONOMIE
10. http://feeds.bbci.co.uk/news/business/rss.xml ECONOMIE
11. http://feeds.reuters.com/reuters/entertainment ART_CULTURE
12. http://feeds.bbci.co.uk/news/entertainment_and_arts/rss.xml ART_CULTURE

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

Hence, the classification can be performed using the concatenation of all textual fields, namely 
```
<title>+<description>+<text>
```
Some of these fields may be missing, in this case they will have a '' value.
  
The <tag> field gives the category that belongs to one of the six categories 
1. 'ART_CULTURE', 
2. 'ECONOMIE/ECONOMY', 
3. 'POLITIQUE/POLITICS', 
4. 'SANTE_MEDECINE/HEALTH_MEDICINE', 
5. 'SCIENCE', 
6. 'SPORT'.

If you use this dataset, please cite:
```P-F.Marteau, N. Béchet and O. Ahmia, Similarité par recouvrement de séquence pour la fouille de données séquentielles et textuelles, 19ème édition de la conférence Extraction et Gestion des Connaissances, EGC 2019, Metz, France.```
