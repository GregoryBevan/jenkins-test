pipeline {
    agent any
    environment {
        VERSION = '1.0.0'
        GIT_USER = credentials('290dbd22-1aa1-40d8-b0ee-88b84c8d5612')
    }
    stages {
        stage('Git tag') {
            steps {
                sh "git config --global user.email 'gregory_bevan@hotmail.com'"
                sh "git config --global user.name $GIT_USER_USR"
                sh "git tag -a $VERSION && git push --tags"
            }
        }
    }
}