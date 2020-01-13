pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(credentials:'aws-credentials', region: 'us-east-1') {
                    s3Upload(file:'index.html', bucket:'jenkins-udacity-project', path:'index.html')
                }
            }
        }
    }
}
