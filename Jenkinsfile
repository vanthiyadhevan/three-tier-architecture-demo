pipeline {
    agent any
    environment {
        DOCKER_IMAGE_CART = 'myapp-cart:latest'
        DOCKER_CATELOG = 'myapp-catalog:latest'
        DOCKER_DISPATCH = 'myapp-dispatch:latest'
        DOCKER_LOAD_GEN = 'myapp-loadgen:latest'
        DOCKER_MONGO = 'myapp-mongo:latest'
        DOCKER_MYSQL = 'myapp-mysql:latest'
        DOCKER_PAYMENT = 'myapp-payment:latest'
        DOCKER_RATING = 'myapp-rating:latest'
        DOCKER_SHIPPING = 'myapp-shipping:latest'
        DOCKER_USER = 'myapp-user:latest'
        DOCKER_WEB = 'myapp-web:latest'
    }
    stages {
        stage('Build Docker & Cart') {
            steps {
                // sh 'tree -a -I Dockerfile .'
                // sh 'ls -l .'
                sh 'docker build -t $DOCKER_IMAGE_CART -f Dockerfile ./cart'
            }
        }

    }
}