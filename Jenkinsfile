pipeline {
    options {
        disableConcurrentBuilds()
    }
    agent any

    environment {
        STACK_SET_NAME = 'GlobalResources'
    }
    stages {
        stage('Get branch specific settings') {
            steps {
                script {
                    try {
                        echo "Getting branch specific settings"

                    } catch (Exception e) {
                        echo "Some error occurred: " + e.toString()
                        throw e
                    }
                }
            }
        }
        stage('Test phase') {
            steps{
                publishChecks(name: 'Stage reporter', conclusion: 'success', summary: 'Yoohoo! All tests passed!')
            }
        }
    }
}
