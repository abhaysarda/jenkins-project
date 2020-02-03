pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(credentials:'jenkins') {
                    s3Upload(file:'index.html', bucket:'jenkins-udacity-abhay')
                }
            }
        }
    }
}