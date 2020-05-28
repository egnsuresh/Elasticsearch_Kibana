# Elasticsearch
* [Schema Creation](#schemacreation)
* [Rename / Alias_name of fields](#rename)


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
