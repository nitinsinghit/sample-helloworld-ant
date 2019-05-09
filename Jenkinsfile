pipeline {  
    agent { label 'redhat_slave1' }
    environment {
        ANT_HOME = tool('MyAnt')
    }
    stages {
        stage("Build") {
            agent { label 'redhat_slave1' }
            steps {
                echo "Building application..."   
                sh '$ANT_HOME/bin/ant clean'
            }
        }
        stage("Unit Tests") {
            steps {
                echo "Unit tests (JUnit)..."
                echo "Mutation tests (pitest)..."

                
            }
        }
        stage("Functional Test") {
            steps {
                echo "Selenium tests..."
            }
        }
        stage("Performance Test") {
            steps {
                echo "JMeter tests..."
            }
        }
        stage("Quality Analysis") {
            steps {
                echo "Running SonarQube..."
            }
        }
        stage("Security Assessment") {
            steps {
                echo "Pen testing..."
            }
        }
        stage("Approval") {
            steps {
                    input "Is the build OK?"
        }
        }
        stage("Deploy") {
            steps {
                echo "Deploying to JBoss 7.2..."
            }
        }
    }
    post {
        always {
        echo "Have a Good Day..."
            }
    }       
}
