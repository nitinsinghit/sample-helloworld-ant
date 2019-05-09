
node ("any")
{

    // Set path for custom management tools on jenkins
    //env.PATH = "${tool 'MyAnt 1.10.5'}/bin:${env.PATH}"
    withAnt(installation: 'MyAnt') {
   // some block
        stage ('Build and Test') {
            sh "ant build clean"
        }  
        
    }  
    
}


