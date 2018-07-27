# Uber-datanalysis - WIP
#This Whole is Split into 2 Phases
#First Phase is Uber-DataAnalysis using Spark MLLIB (KMeans Algorithms best suited)and Prediction using KMeans.
#Second Phase is Rules Implementation using RHDM and Firing the rules to detect the Surge Prediction, it uses Kafka and Spark Streaming.
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
 
 
    
 
    
 
    
 
 

   


   
   
