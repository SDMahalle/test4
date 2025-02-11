pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo "Build Started"
            }
        }
        stage('Test') {
            steps {
                echo "Test Execution Started"
            }
        }
        stage('Deliver for development') {

                    steps {
                        echo "Deliver for development"
                        input message: 'Finished using the web site? (Click "Proceed" to continue)'
                        echo "Delivery for developement end"
                    }
                }
                stage('Deploy for production') {

                    steps {
                        echo "Deliver for production"
                                               input message: 'Finished using the web site? (Click "Proceed" to continue)'
                                               echo "Delivery for production end"
                    }
                }
    }
}