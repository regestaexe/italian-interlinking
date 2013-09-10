italian-interlinking
====================
Some resources to make interlinking of RDF resources easier, especially for italian people

LikedGeoData
------------

we extracted the italian places from http://linkedgeodata.org/sparq
<pre>
CONSTRUCT {?a ?b ?c}
FROM <http://linkedgeodata.org>
WHERE {
   ?a a <${class}>; <http://linkedgeodata.org/property/is_in> ?IN .
   FILTER(REGEX(?IN,'Italy')) .
   ?a ?b ?c
}
</pre>

*the classes*
*http://linkedgeodata.org/ontology/City
*http://linkedgeodata.org/ontology/Town
*http://linkedgeodata.org/ontology/Suburb
*http://linkedgeodata.org/ontology/Place
*http://linkedgeodata.org/ontology/Village
