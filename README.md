# knowledge-graph-api

## Freebase

Further background on Freebase and the deprecated Freebase APIs is available in my [freebase-mql](https://github.com/nchah/freebase-mql) repository. The KG API is a successor to the functionality once offered by the Freebase APIs.

## Google Knowledge Graph

Google's Knowledge Graph is an internal knowledge base of linked data that draws from a wide range of sources for its data. The aforementioned Freebase database was one of the data sources. 

The Knowledge Graph allows the search engine to serve up the rich Knowledge Cards that take up the right side of many notable search results.

The current KG API has more limited search capabilities compared to the previous Freebase API. It's currently not possible to craft queries (as was done in MQL) that return a sub-graph of Freebase topics. The best alternative will be to use the unique identifier (Freebase mid) and join it with other data, such as the growing volume on Wikidata.

An example query:
```
$ python kg-api.py 'google'
Google
 - entity_types: Thing, Organization, Corporation
 - description: Technology company
 - detailed_description: Google is an American multinational technology company specializing in Internet-related services and...
 - identifier: kg:/m/045c7b
 - url: N/A
 - resultScore: 287.675293

Google X
 - entity_types: EducationalOrganization, Corporation, Organization, Thing
 - description: Corporation
 - detailed_description: X, previously Google X, is a semi-secret research and development facility created by Google and ope...
 - identifier: kg:/m/0hhrhd0
 - url: N/A
 - resultScore: 47.670715

Googleplex
 - entity_types: Thing, Place
 - description: Building complex
 - detailed_description: The Googleplex is the corporate headquarters complex of Google, Inc., located at 1600 Amphitheatre P...
 - identifier: kg:/m/03bby1
 - url: http://www.google.com/about/jobs/locations/mountain-view/
 - resultScore: 44.866741

```


## Sources

### Announcements

Many Freebase and Knowledge Graph related updates are posted on the once active [freebase-discuss](https://groups.google.com/forum/#!forum/freebase-discuss) Google Group and the [Google+](https://plus.google.com/u/0/109936836907132434202/posts) community.

- Jul 16, 2010 (joining Google) https://groups.google.com/d/msg/freebase-discuss/NkCF1DayKzA/QQufQ9gDwBsJ
- Dec 16, 2014 (timeline for Freebase sunsetting announced) https://plus.google.com/u/0/109936836907132434202/posts/bu3z2wVqcQc and https://groups.google.com/d/msg/freebase-discuss/s_BPoL92edc/Y585r7_2E1YJ
- Mar 26, 2015 (details on Wikidata and new KG API projected) https://plus.google.com/u/0/109936836907132434202/posts/3aYFVNf92A1
- Sep 28, 2015 (short update on KG API) https://plus.google.com/u/0/109936836907132434202/posts/3aYFVNf92A1
- Dec 16, 2015 (KG Search API releasted) https://plus.google.com/u/0/109936836907132434202/posts/iY8NZGFF6DN
- Jan 28, 2016 (KG Search Widget released) https://plus.google.com/u/0/109936836907132434202/posts/MCKpjUpx1H1
- May 02, 2016 (Freebase.com shutdown) https://groups.google.com/forum/#!topic/freebase-discuss/WEnyO8f7xOQ

### Freebase

- http://www.freebase.com/ (shutdown on May 02, 2016, now redirects to the data dumps)
- http://wiki.freebase.com/wiki/Main_Page

### Knowledge Graph

- https://en.wikipedia.org/wiki/Knowledge_Graph
- https://googleblog.blogspot.ca/2012/05/introducing-knowledge-graph-things-not.html (May 16, 2012 official KG announcement)
- https://www.google.com/intl/bn/insidesearch/features/search/knowledge.html (Google Inside Search explaining the Knowledge Graph)
- http://searchengineland.com/laymans-visual-guide-googles-knowledge-graph-search-api-241935 (Search Engine Land provides a good tutorial)

### Google Developers Resources

**Freebase APIs**
- https://developers.google.com/freebase/
- https://developers.google.com/freebase/mql/

**Knowledge Graph Search APIs**
- https://plus.google.com/109936836907132434202/posts/iY8NZGFF6DN (released on Dec 16, 2015)
- https://developers.google.com/knowledge-graph/
- https://developers.google.com/knowledge-graph/reference/rest/v1/ (entities.search method's parameters)


