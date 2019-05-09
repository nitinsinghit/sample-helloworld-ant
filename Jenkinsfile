
node ("redhat-slave1")
{

    // Set path for custom management tools on jenkins
    //env.PATH = "${tool 'MyAnt 1.10.5'}/bin:${env.PATH}"
    withAnt(installation: 'MyAnt') {
   // some block
        stage ('Build and Test') {
            sh "ant -f build.xml clean"
        }  
        
    }  
    
}


