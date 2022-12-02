# NYC-AccidentAnalysis

## Getting the Data

Download the dataset from : [NYC Dataset](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)

## Elasticsearch

1. Install the open source version of elasticsearch : https://www.docker.elastic.co/r/elasticsearch/elasticsearch-oss:6.7.2
2. Check if elasticsearch is running on http://localhost:9200/ by using the command /bin/elasticsearch
3. We need to ingest our data in elasticsearch so that elasticseearch will index the data.

## Kibana

1. Intall the open source versions of Kibana : https://www.docker.elastic.co/r/kibana/kibana-oss:6.7.2
2. Check if Kibana is running on http://localhost:5601/ by using the command /bin/kibana

## Filebeat

1.  Intall the open source versions of Filebeat : https://www.docker.elastic.co/r/kibana/kibana-oss:6.7.2
2.  We will use Filebeat to collect the data from the source and ingest it into elasticsearch for indexing.








Steps to run -

1. Download the dataset from - [NYC Dataset](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)

2. Intall the open source versions of elasticsearch, Kibana and Filebeat.

    Elasticsearch - https://www.docker.elastic.co/r/elasticsearch/elasticsearch-oss:6.7.2
    
    Kibana - https://www.docker.elastic.co/r/kibana/kibana-oss:6.7.2
    
    Filebeat - https://www.docker.elastic.co/r/beats/filebeat-oss:6.7.2
    
3. Check if elasticsearch is running on http://localhost:9200/ by using the command /bin/elasticsearch

4. Check if Kibana is running on http://localhost:5601/ by using the command /bin/kibana

5. Create a pipeline in Kibana Dev tab - pipeline.txt

6. 
