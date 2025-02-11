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

                    steps {
                        echo "Deliver for production"

                                               echo "Delivery for production end"
                    }
                }

          stage('Update POM') {
                                     steps {
                                         sh '''
                                             # Clone the test2 repository
                                              echo "repo cloning started"
                                             rm -rf test5
                                             git clone https://github.com/SDMahalle/test5.git
                                             cd test5
                                             echo "navigated to test 4"
                                             # Checkout the main branch
                                             git checkout main
                                             echo "checked out main branch"
                                             # Make changes to the pom.xml file
                                             # (Assuming you have a script or command to update the pom.xml)
                                             # For example, using sed to update a version number
                                           #update version in pom.xml here
                                           # Ensuring the running directory has pom.xml
                                                                ls -l pom.xml
                                                               # Updating version using sed

                                                                sed -i "" "s/<version>.*</version>/<version>$1.1-SNAPSHOT</version>/" pom.xml
                                                               # Verify sed operation success
                                                                grep "1.1-SNAPSHOT" pom.xml
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
}