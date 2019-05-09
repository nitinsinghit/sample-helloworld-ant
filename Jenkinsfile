pipeline {  
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building application..."   
                sh "tool 'MyAnt' clean"
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
        jecho "Have a Good Day..."
            }
    }       
}
