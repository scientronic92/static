pipeline {
    agent any
    stages {
        stage('Linting') {
            steps {
                sh tidy -q -e *.html
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1', credentials:'aws-static') {
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-udacity-project')
                }
            }
        }
    }
}
