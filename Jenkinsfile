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

        DOCKER_REPO_NAME = 'vanthiyadevan' // Replace with your Docker registry
    }
    stages {
        stage('Build Docker & Cart') {
            steps {
                sh 'docker build -f ./cart/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_IMAGE_CART}:${BUILD_ID} ./cart'
            }
        }
        stage('Build Docker & Catalog') {
            steps {
                sh 'docker build -f ./catalog/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_CATELOG}:${BUILD_ID} ./catalogue'
            }
        }
        stage('Build Docker & Dispatch') {
            steps {
                sh 'docker build -f ./dispatch/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_DISPATCH}:${BUILD_ID} ./dispatch'
            }
        }
        stage('Build Docker & Load Gen') {
            steps {
                sh 'docker build -f ./loadgen/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_LOAD_GEN}:${BUILD_ID} ./load-gen'
            }
        }
        stage('Build Docker & Mongo') {
            steps {
                sh 'docker build -f ./mongo/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_MONGO}:${BUILD_ID} ./mongo'
            }
        }
        stage('Build Docker & MySQL') {
            steps {
                sh 'docker build -f ./mysql/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_MYSQL}:${BUILD_ID} ./mysql'
            }
        }
        stage('Build Docker & Payment') {
            steps {
                sh 'docker build -f ./payment/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_PAYMENT}:${BUILD_ID} ./payment'
            }
        }
        stage('Build Docker & Rating') {
            steps {
                sh 'docker build -f ./rating/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_RATING}:${BUILD_ID} ./ratings'
            }
        }
        stage('Build Docker & Shipping') {
            steps {
                sh 'docker build -f ./shipping/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_SHIPPING}:${BUILD_ID} ./shipping'
            }
        }
        stage('Build Docker & User') {
            steps {
                sh 'docker build -f ./user/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_USER}:${BUILD_ID} ./user'
            }
        }
        stage('Build Docker & Web') {
            steps {
                sh 'docker build -f ./web/Dockerfile -t ${DOCKER_REPO_NAME}/${DOCKER_WEB}:${BUILD_ID} ./web'
            }
        }
        stage('Push Docker Images') {
            steps {
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_IMAGE_CART}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_CATELOG}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_DISPATCH}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_LOAD_GEN}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_MONGO}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_MYSQL}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_PAYMENT}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_RATING}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_SHIPPING}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_USER}:${BUILD_ID}'
                sh 'docker push ${DOCKER_REPO_NAME}/${DOCKER_WEB}:${BUILD_ID}'
            }
        }

    }
}