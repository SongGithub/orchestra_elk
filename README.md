#
orchestra_elk

![alt text](http://cdn0.wideopenspaces.com/wp-content/uploads/2014/09/Bull-Elk-Bugling.jpg)

A demo project to orchestrate the ELK(ElasticSearch Logstash and Kibana) stack with docker/docker-compose
> "What I can't build, I don't really understand."

# Goal
- run the ELK stack with persistent storage of logs.

# Usage

Start the ELK stack using *Docker-Compose*
```bash
$ docker-compose up
```

## Stack's ports:
- 5000: Logstash TCP input
- 5601: Kibana for data visualization
- 9200: ElasticSearch HTTP
- 9300: ElasticSearch TCP

## Visualize data:
visit the browser at URL `localhost:5601`

# Persist ElasticSearch data: 
postgres has been supplied to store data.

# Basic tuning
- users can allocate more/less memory by tunning var `ES_JAVA_OPS`, default is 1 GB

# TODO
- fine-tune the kibana and elastic search to perform
- configure logstash to receive testing data.