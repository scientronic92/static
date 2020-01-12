pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(credentials:'IDofAwsCredentials') {
                    s3Upload(file:'index.html', bucket:'jenkins-udacity-project', path:'static/index.html')
                }
            }
        }
    }
}
