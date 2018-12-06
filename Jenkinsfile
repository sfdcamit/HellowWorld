pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is build Stage"
            }
        }
        stage('Test') { 
            steps {
                input('do you want to proceed?)
            }
        }
        stage('Stage Four'){
            parallel{
                stage('unit test'){
                    steps{
                        echo "unit tes is running"
                    }
                }
                stage('Integration Test'){
                    steps{
                        echo "Integration Test is running"
                    }
                }
            }
        }
        stage('Deploy') { 
            steps {
                echo "This is Deploy Stage" 
            }
        }
    }
}
