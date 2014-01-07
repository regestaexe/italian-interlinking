italian-interlinking
====================
Some resources to make interlinking of RDF resources easier, especially for italian people

LikedGeoData
------------

we extracted the italian places from http://linkedgeodata.org/sparql using a script based on this query:
```
CONSTRUCT {?a ?b ?c}
FROM <http://linkedgeodata.org>
WHERE {
   ?a a <${class}>; 
   ?b ?c; 
   <http://linkedgeodata.org/property/is_in> ?IN.
   FILTER(REGEX(?IN,'Italy'))
 }
```

**the classes**  
* http://linkedgeodata.org/ontology/City
* http://linkedgeodata.org/ontology/Town
* http://linkedgeodata.org/ontology/Suburb
* http://linkedgeodata.org/ontology/Place
* http://linkedgeodata.org/ontology/Village


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/regestaexe/italian-interlinking/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

