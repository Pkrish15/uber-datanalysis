# uber-datanalysis - WIP
1) Implementation on Openshift <br>
   oc new-project pk-zp <br> <br>
   oc create -f https://raw.githubusercontent.com/Pkrish15/uber-datanalysis/master/zeppelin-openshift.yaml <br> <br>
   oc new-app --template=$namespace/apache-zeppelin-openshift \
    --param=APPLICATION_NAME=apache-zeppelin \
    --param=GIT_URI=https://github.com/rimolive/zeppelin-notebooks.git \
    --param=ZEPPELIN_INTERPRETERS=md       <br><br>
    
   


   
   
