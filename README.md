# NYC-AccidentAnalysis

## Getting the Data

Download the dataset from : [NYC Dataset](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)

## Elasticsearch

1. Install the open source version of elasticsearch : https://www.docker.elastic.co/r/elasticsearch/elasticsearch-oss:6.7.2
2. Check if elasticsearch is running on http://localhost:9200/ by using the command /bin/elasticsearch
3. We need to ingest our data in elasticsearch so that elasticseearch will index the data.

## Kibana

1. Install the open source versions of Kibana : https://www.docker.elastic.co/r/kibana/kibana-oss:6.7.2
2. Check if Kibana is running on http://localhost:5601/ by using the command /bin/kibana

## Filebeat

1.  Install the open source versions of Filebeat : https://www.docker.elastic.co/r/kibana/kibana-oss:6.7.2
2.  We will use Filebeat to collect the data from the source and ingest it into elasticsearch for indexing.
3.  We will also create a yml file in filebeat to create the schema for indexing and to convert our CSV format data to JSON format as elasticsearch only accepts JSON format.

## Creating a Pipeline
Go to the development tab in Kibana and create a pipeline to ignore all the missing and incorrect values. (copy the text in pipeline.txt in the kibana dev tab).


## Ingesting the data

1. Add the filebeat_nypd.yml file and csv format dataset to the filebeat folder.
2. Run filebeat and start ingesting the data into the elasticsearch.
3. Check the Kibana tab for the records ingested and once the records have been ingested it will show information about the data.

## Insights
1. After the data has been ingested in the elasticsearch, elasticsearch will index the data.
2. We will gain insights and create visualizations using the kibana visulaize tab. 








