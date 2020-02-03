pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                tidy -q -e *.html
                withAWS(credentials:'jenkins') {
                    s3Upload(file:'index.html', bucket:'jenkins-udacity-abhay')
                }
            }
        }
    }
}