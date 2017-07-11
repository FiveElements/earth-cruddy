
# earth-editable-layout


The earth-editable-layout for an layout usable for edition like air-cruddy component

Respect the material design https://material.io/guidelines/components/buttons.html#buttons-dropdown-buttons



## Insert Mapping
```bash
curl -XDELETE 'localhost:9200/5elements?pretty'
```
 

```bash
curl -XPUT 'http://localhost:9200/5elements?pretty' -H 'Content-Type: application/json' -d'
{
  "mappings": {
    "5elements": { 
      "_all":       { "enabled": false  }, 
      "properties": { 
        "title":    { "type": "text"  }, 
        "name":     { "type": "text"  }, 
        "age":      { "type": "integer" }  
      }
    } 
    }
  }
}
'
```
 
## Insert Data

```bash
curl -XPUT 'http://localhost:9200/5elements/5elements/1?pretty' -d'{ "firstname" : "Liloo",  "lastname" : "Dallas" }'
```
 