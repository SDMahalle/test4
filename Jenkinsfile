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

                        echo "Delivery for developement end"
                    }
                }
                stage('Deploy for production') {

                    sh '''
                                                       # Clone the test2 repository
                                                        echo "repo cloning started"
                                                       git clone https://github.com/SDMahalle/test3.git
                                                       cd test3
                                                       echo "navigated to test 3"
                                                       # Checkout the main branch
                                                       git checkout main
                                                       echo "checked out main branch"
                                                       # Make changes to the pom.xml file
                                                       # (Assuming you have a script or command to update the pom.xml)
                                                       # For example, using sed to update a version number
                                                       sed -i 's/<version>1.0-SNAPSHOT</version>/<version>1.1-SNAPSHOT</version>/' pom.xml
                                                       echo "updated pom version"
                                                       # Commit and push the changes
                                                       git config user.name "sagarmahalle88@gmail.com"
                                                       git config user.email "sagarmahalle88@gmail.com"
                                                       git add pom.xml
                                                       git commit -m "Update pom.xml version"
                                                       echo "commit updated pom.xml"
                                                       git push origin main
                                                       echo "push updated pom.xml"
                                                   '''
                }
    }
}