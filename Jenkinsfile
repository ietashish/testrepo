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
                publishChecks name: 'example', title: 'Pipeline Check', summary: 'check through pipeline',
    text: 'you can publish checks in pipeline script',
    detailsURL: 'https://github.com/jenkinsci/checks-api-plugin#pipeline-usage',
    actions: [[label:'an-user-request-action', description:'actions allow users to request pre-defined behaviours', identifier:'an unique identifier']]

            }
        }
    }
}
