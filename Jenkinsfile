pipeline {
    agent any
    environment {
        VERSION = '1.0.0'
    }
    stages {
        stage('Git tag') {
            steps {
                sh "git tag -a $VERSION && git push --tags"
            }
        }
    }
}