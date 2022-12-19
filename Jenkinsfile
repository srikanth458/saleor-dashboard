pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/WorkshopsByKhaja/saleor-dashboard.git'
            }
        }
        stage('docker image build') {
            steps {
                sh 'docker image build -t srikanth458/images:image1 .'
            }
        }
        stage('push image to registry') {
            steps {
                sh 'docker push srikanth458/images:image1'
            }
        }
    }
}
