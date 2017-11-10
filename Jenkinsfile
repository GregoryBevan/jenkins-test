pipeline {
    agent any
    environment {
        VERSION = '1.0.0'
        GIT_USER = credentials('290dbd22-1aa1-40d8-b0ee-88b84c8d5612')
    }
    stages {
        stage('Git tag') {
            steps {
                withCredentials([usernamePassword(credentialsId: '290dbd22-1aa1-40d8-b0ee-88b84c8d5612', 
                                                  passwordVariable: 'GIT_PWD', 
                                                  usernameVariable: 'GIT_USR')]) {
                    sh "git config --global user.email 'gregory_bevan@hotmail.com'"
                    sh "git config --global user.name $GIT_USR"
                    sh "git remote set-url origin https://$GIT_USR:$GIT_PWD@github.com/GregoryBevan/jenkins-test.git"
                    sh "git tag -d $VERSION && git tag -a $VERSION -m 'Release $VERSION' && git push --tags"
                }
            }
        }
    }
}