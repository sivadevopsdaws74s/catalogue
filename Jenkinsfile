#!groovy
// it means the libraries will be downloaded and accessible at run time
@Library('roboshop-shared-library') _

def configMap = [
    application: "nodeJSEKS", // we are migrating monolithic to Microservice
    component: "catalogue"
]
env

// this is .groovy file name and function inside it
//if not master then trigger pipeline
if ( ! env.BRANCH_NAME.equalsIgnoreCase('master')){
    pipelineDecission.decidePipleine(configMap)
}
else{
    echo "master PROD deployment should happen through CR"
}

