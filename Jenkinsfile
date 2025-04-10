pipeline {
    agent any
    parameters {
        string(name: 'GREETING', defaultValue: 'Hello', description: 'The greeting message')
        choice(name: 'BRANCH', choices: ['master', 'dev'], description: 'Branch to build')
    }
    stages {
         stage('Checkout') {
            steps {
                git url: 'https://github.com/PeterPorzuczek/TimeRiddle.git', branch: 'master'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                // Tutaj mogą znaleźć się komendy budujące twoją aplikację, np. mvn clean install
            }
        }
        stage('Example') {
            steps {
                echo "${params.GREETING}, we are building the ${params.BRANCH} branch."
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // Komendy uruchamiające testy, np. mvn test
            }
        }
        stage('Deploy') {
            when {
                expression { params.DEPLOY }
            }
            steps {
                echo 'Wdrażanie aplikacji...'
            }
        }
    }
}
