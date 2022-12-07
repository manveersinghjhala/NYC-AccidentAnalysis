# NYC-AccidentAnalysis

## Getting the Data

Download the dataset from : [NYC Dataset](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)

## Elasticsearch

1. Install the open source version of elasticsearch : https://www.docker.elastic.co/r/elasticsearch/elasticsearch-oss:6.7.2
2. Check if elasticsearch is running on http://localhost:9200/ by using the command /bin/elasticsearch
3. We need to ingest our data in elasticsearch so that elasticsearch will index the data.

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

Here are few examples of the insights we gained - 

1. Major causes of accidents:

<img width="825" alt="Screen Shot 2022-11-15 at 10 01 36 AM" src="https://user-images.githubusercontent.com/69818630/206072322-6ad51d69-8aad-42f6-baf1-99badc999016.png">

2. Major hotspots of accidents:

<img width="860" alt="Screen Shot 2022-11-15 at 9 59 57 AM" src="https://user-images.githubusercontent.com/69818630/206072493-88d2c62d-0bc9-400d-b346-20873c2bc80f.png">

3. Type of vehicles that are involved in most accidents:

<img width="894" alt="Screen Shot 2022-11-15 at 9 57 35 AM" src="https://user-images.githubusercontent.com/69818630/206072708-87cf667c-6160-4f64-959e-042e1e016ad3.png">

4. Areas where most number of accidents occur:

<img width="874" alt="Screen Shot 2022-11-15 at 9 58 36 AM" src="https://user-images.githubusercontent.com/69818630/206072846-44e087ac-13ad-4246-845a-48d3ba348218.png">






