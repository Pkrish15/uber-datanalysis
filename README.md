# Data Discovery Phase  - First Phase
# This Whole is Split into 2 Phases <br> <br>
#The example data set is Uber trip data, which FiveThirtyEight obtained from the NYC Taxi & Limousine Commission. In this example, we will discover the clusters of Uber data based on the longitude and latitude, then we will analyze the cluster centers by date/time. The data set has the following schema:

The Data Set Schema
Date/Time: The date and time of the Uber pickup
Lat: The latitude of the Uber pickup
Lon: The longitude of the Uber pickup
Base: The TLC base company affiliated with the Uber pickup
​​The Data Records are in CSV format. An example line is shown below:

2014-08-01 00:00:00,40.729,-73.9422,B02598


# Second Phase is Analytics using the Model which involves Rules Implementation using RHDM and Firing the rules to detect the Surge Prediction, it uses Kafka and Spark Streaming.<br>
1) Implementation on Openshift <br>
   a) oc new-project pk-zp <br> <br>
   b) oc create -f https://raw.githubusercontent.com/Pkrish15/uber-datanalysis/master/zeppelin-openshift.yaml <br> <br>
   c) oc new-app --template=$namespace/apache-zeppelin-openshift \
    --param=APPLICATION_NAME=apache-zeppelin \
    --param=GIT_URI=https://github.com/rimolive/zeppelin-notebooks.git \
    --param=ZEPPELIN_INTERPRETERS=md       <br><br>
 
 2) Create a PVC in the pod claiming 2GiB <br><br>
 3) Copy the Local Data to the Pod Directory using Rsync Command <br><br>
     oc rsync /home/prakrish/workspace/uberdata-analysis/src/main/resources/data/  apache-zeppelin-2-f89tz:/data <br>
     oc rsync src directory pod directory:/data This is a format <br> <br>
 
 4) Open the Zeppellin notebook <br> <br>
    oc get route <br>
    http://apache-zeppelin-pk-zp.apps.dev39.openshift.opentlc.com/#/
    
 5) Import the JSON Notebook in the Zepplin Notebook <br> <br>
    Currently it is in our GitHub URL <br>
    https://raw.githubusercontent.com/Pkrish15/uber-datanalysis/master/Uber%20Data%20Analysis.json <br> <br>
    
 6) Run the Zepplin Notebook at every stages, Please read the zepplin tutorial if required. <br> <br>
 
#  Analytics using the model which involved Spark Streaming and Rules Implementation - 2nd Phase (Work in Progress)

#  Detailed Explaination of the first phase - Data Discovery Phase

1) Why this phase is needed? <br>
   This phase is needed to study about the historical data, and observe the pattern recognition of the uber system which is needed. Based on this we can arrive a conclusion for better decision making and predictions.<br>
 
 2) What is analytics using the model? <br>
   This is the second phase of the project,uses the model in production on live events, it still needed to do an analyis of historical data. <br>
   
   
   
 
 
    
 
    
 
    
 
 

   


   
   
