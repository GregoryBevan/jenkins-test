pipeline {
    agent any
    environment {
        VERSION = '1.0.0'
    }
    stages {
        stage('Git tag') {
            steps {
                sh "git tag -d $VERSION && git push --tags"
            }
        }
    }
}