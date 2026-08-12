splunk v:1 



I. the Splunk Platform

&#x09;

1. what is splunk 

   1. big data platform for machine data
   2. convert raw unstructured data into searchable events 
   3. organize in indexes
   4. users can create dashboard, alerts, and reports 
2. what is machine data 

   1. Digital exhaust produced by server, application, and , network devices
   2. eg: web access logs, application logs, windows event logs, network packet capture, OS performance metrics
3. problems with machine data

   1. volume
   2. velocity
   3. unstructured
   4. Distributed
4. Spunk to rescue

   1. Splunk indexes data from any source to enable searching, reporting and visualizing at scale 
5. Splunk Architecture

   1. sources: machine data  -> splunk universal forwarder" "TCP/HTTPS" " : splunkd-> splunk indexer -> TCP <- splunk search head <-HTTPS <- splunk user
   2. indexer:

      1. Receives data from client
      2. converts raw data to searchable events
      3. execute searches
   3. search head

      1. GUI for the user
      2. manage Searches 
      3. Distribute searches to indexers 
      4. maintains access control
   4. universal forwarder

      1. collects data  from machine data host
      2. keep track of data ingestion
      3. very lightweight and production ready
   5. inside an indexer 

      1. Splunk stores data in indexes
      2. indexes contain data buckets 
      3. data buckets contain raw data and index files 
      4. data retention policies are configured at index level
   6. data buckets life cycle

      1. hot -> warm -> cold -> Frozen (Archive/ delete)
      2. hot bucket 

         1. contains newest data
         2. open for both read and write
         3. Splunk admin can configure when to roll data to warm bucket
      3. warm bucket 

         1. open for read only no write
         2. hot and warm buckets are kept in faster storage 
         3. when data age, it is rolled to cold from warm bucket
      4. cold bucket

         1. open for read only 
         2. cold buckets can be kept in cheaper storage
         3. depending on the config, data  from cold buckets can either be deleted or archived to frozen bucket
      5. frozen bucket 

         1. data is not searchable 
         2. data needs to be thawed first using splunk script to make it searchable
   7. splunk security 

      1. Splunk implements RBAC(role based access control)
      2. three primary roles : user, power, Admin
      3. power user can share knowledge objects
      4. for Splunk user, knowledge objects are private
      5. knowledge objects 

         1. field extractions
         2. lookups
         3. data models
         4. tags
   8. other Splunk component 

      1. deployment server
      2. license master
      3. heavy forwarder
      4. monitoring console 
      5. search head deployer



&#x20;

&#x20;

