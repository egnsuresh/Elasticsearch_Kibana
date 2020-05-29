# Elasticsearch
click on any one of below to go directly to that section
* [Schema Creation](#schemacreation)
* [Rename / Alias_name of fields](#rename)
* [Search with multiple values](#search_with_multi_term): similar to IN in SQL

search_with_multi_term
<div id="schemacreation">
<h5>Schema Creation<h5>
<ul>
  <li>using PUT</li>
  <li>
  example:
   <pre>
  <code>
 PUT myindexnameasuser
{
  "mappings": {
      "properties": {
        "name" : {
          "properties" : {
            "first" : {
              "type" : "text"
            },
            "last" : {
              "type" : "text"
            }
          }
        },
        "id": { "type": "keyword" },
        "email": { "type": "keyword" },
        "cretion_date": { "type": "date" }
      }
  }
}
</code>
</pre>
</li>
  
  </ul>
</div>
<div id="rename">
<h5>Rename or Alias_name of field<h5>
<ul>
  <li>using PUT</li>
  <li>
  example:
  <pre>
  <code>
 PUT myindexnameasuser
{
  "mappings": {
      "properties": {
        "name" : {
          "properties" : {
            "first" : {
              "type" : "text"
            },
            "last" : {
              "type" : "text"
            }
          }
        },
        "id": { "type": "keyword" },
        "email": { "type": "keyword" },
        "cretion_date": { "type": "date" }
      } 
  }
}
  </code>
  </pre>
  </li>
  </ul>
</div>
  
<div id="search_with_multi_term">
<h5>Search with multi terms<h5>
  should: for to check all 
<ul>
  <li>using PUT</li>
  <li>
  example:
   <pre>
  <code>
 GET users
{
 "bool" : {
   "should" : [ {
     "terms" : {
       "name" : [ "abcd", "xyz" ]
     }
   }, {
     "terms" : {
       "id" : [ "1001","1002" ]
     }
   } ]
 }
</code>
</pre>
</li>
  
  </ul>
</div>
