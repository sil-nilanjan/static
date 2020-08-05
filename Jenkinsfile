pipeline {
    agent any
    stages {
        stage ('Upload to AWS'){
            steps {
                withEnv(["AWS_ACCESS_KEY_ID=${env.AWS_ACCESS_KEY_ID}",
                         "AWS_SECRET_ACCESS_KEY=${env.AWS_SECRET_ACCESS_KEY}",
                         "AWS_DEFAULT_REGION=${env.AWS_DEFAULT_REGION}"]) {
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file: 'index.html', bucket: 'udacity-assignment-pipeline')
                }
            }
        }
    }
}
