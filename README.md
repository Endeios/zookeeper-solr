# Zookeeper and Solr

Follows a curated guide to understanding and deploying Solr and Zookeeper, in spring java springboot souce.

## What is Zookeeper

```Provides distributed coordination and synchronization of settings, state of some application state```

But what does it mean? Many of us had this problem: 

```I have a nice application, now I need to have it distribuited, so I can scale.``` 

![](diagrams/out/apps-with-state.png)

And the following question is: 

```How do I distribuite the state of my application to guarantee hig availability and the state always updated?```

We all know that the issue here is about maitaining that distribuited state, and we all know that is a steaming mess of issues and retries, and connections and corner cases

![](diagrams/out/apps-with-state-no-zk.png)

Zookeeper answers to that problem:  it keeps the STATE of a distributed application. It also offers _high availability_ to your distributed application, in the same library: if one

- Keeps the state of the app on ZK
- Sets ZK in a way that "MAKES SENSE" (more on this later)

then has solved the problem of distribuiting a state for an app.
![](diagrams/out/apps-with-state-zk.png)

# Links and sources
- https://solr.apache.org/guide/8_8/solr-tutorial.html
- https://github.com/docker-solr/docker-solr
- https://javadeveloperzone.com/solr/solr-tutorial/
- http://www.solrtutorial.com/solrj-tutorial.html
- https://riptutorial.com/solrj
- https://www.youtube.com/watch?v=Zw4M4NGv-Rw
- https://stackoverflow.com/questions/59943241/zookeeper-admin-server-port
- https://lucidworks.com/post/understanding-transaction-logs-softcommit-and-commit-in-sorlcloud/
- https://solr.apache.org/guide/8_8/setting-up-an-external-zookeeper-ensemble.html
- https://zookeeper.apache.org/doc/r3.4.10/zookeeperAdmin.html
- https://solr.apache.org/guide/6_6/updatehandlers-in-solrconfig.html
- https://stackoverflow.com/questions/6954358/how-to-optimize-solr-index
- https://cwiki.apache.org/confluence/display/solr/FAQ#How_can_I_delete_all_documents_from_my_index.3F
- https://lastfiascorun.com/cities/often-asked-how-do-you-purge-messages-in-rabbitmq.html
- https://facingissuesonit.com/2020/03/29/spring-boot-data-configuration-properties-and-default-value/
- https://docs.spring.io/spring-boot/docs/1.4.x/reference/html/common-application-properties.html