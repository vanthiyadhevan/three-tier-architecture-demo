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

        DOCKER_REGISTRY_NAME = 'vanthiyadevan' // Replace with your Docker registry
    }
    stages {
        stage('Build Docker & Cart') {
            steps {
                sh 'docker build -f ./cart/Dockerfile -t ${DOCKER_IMAGE_CART}  ./cart'
            }
        }
        stage('Build Docker & Catalog') {
            steps {
                sh 'docker build -f ./catalog/Dockerfile -t ${DOCKER_CATELOG}  ./catalog'
            }
        }
        stage('Build Docker & Dispatch') {
            steps {
                sh 'docker build -f ./dispatch/Dockerfile -t ${DOCKER_DISPATCH}  ./dispatch'
            }
        }
        stage('Build Docker & Load Gen') {
            steps {
                sh 'docker build -f ./loadgen/Dockerfile -t ${DOCKER_LOAD_GEN}  ./loadgen'
            }
        }
        stage('Build Docker & Mongo') {
            steps {
                sh 'docker build -f ./mongo/Dockerfile -t ${DOCKER_MONGO}  ./mongo'
            }
        }
        stage('Build Docker & MySQL') {
            steps {
                sh 'docker build -f ./mysql/Dockerfile -t ${DOCKER_MYSQL}  ./mysql'
            }
        }
        stage('Build Docker & Payment') {
            steps {
                sh 'docker build -f ./payment/Dockerfile -t ${DOCKER_PAYMENT}  ./payment'
            }
        }
        stage('Build Docker & Rating') {
            steps {
                sh 'docker build -f ./rating/Dockerfile -t ${DOCKER_RATING}  ./rating'
            }
        }
        stage('Build Docker & Shipping') {
            steps {
                sh 'docker build -f ./shipping/Dockerfile -t ${DOCKER_SHIPPING}  ./shipping'
            }
        }
        stage('Build Docker & User') {
            steps {
                sh 'docker build -f ./user/Dockerfile -t ${DOCKER_USER}  ./user'
            }
        }
        stage('Build Docker & Web') {
            steps {
                sh 'docker build -f ./web/Dockerfile -t ${DOCKER_WEB}  ./web'
            }
        }
        stage('Push Docker Images') {
            steps {
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_IMAGE_CART}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_CATELOG}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_DISPATCH}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_LOAD_GEN}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_MONGO}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_MYSQL}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_PAYMENT}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_RATING}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_SHIPPING}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_USER}'
                sh 'docker push ${DOCKER_REGISTRY_NAME}/${DOCKER_WEB}'
            }
        }

    }
}