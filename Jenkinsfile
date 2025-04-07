pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Tutaj mogą znaleźć się komendy budujące twoją aplikację, np. mvn clean install
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // Komendy uruchamiające testy, np. mvn test
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                // Skrypty do deploymentu aplikacji
            }
        }
    }
}
