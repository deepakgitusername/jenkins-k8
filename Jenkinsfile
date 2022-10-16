pipeline {
    agent {
        label 'linux2'
    }
    environment {
        KUBECONFIG_FILE = credentials('my-kubeconfig')
    }
    stages {
        stage('Deploying applications') {
            steps {
                sh 'echo "Deploying Application"'
                sh '''
                kubectl --kubeconfig $KUBECONFIG_FILE apply -f httpd-deploy.yaml       
                '''
            }
        }
        }
}