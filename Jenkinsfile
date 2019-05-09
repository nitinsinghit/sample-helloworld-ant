
node ("redhat-slave1")
{

    // Set path for custom management tools on jenkins
    env.PATH = "${tool 'MyAnt 1.10.5'}/bin:${env.PATH}"

    try {

        stage ("Clean") {
            sh 'ant -f build.xml clean'
        }      

    }
    catch(e) {

        throw e
    }
    
}


