pipeline {
    agent any
    stages {
        stage('Checkout K8s Configs') {
            steps {
                git branch: 'main', url: 'https://github.com/nikhilmathur1957/learner-report-k8s.git'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh '''
                kubectl apply -f backend-deployment.yaml
                kubectl apply -f backend-service.yaml
                kubectl apply -f frontend-deployment.yaml
                kubectl apply -f frontend-service.yaml
                kubectl apply -f mongodb-deployment.yaml
                kubectl apply -f configmaps.yaml
                '''
            }
        }
    }
}
