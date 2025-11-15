pipeline {
    agent any
    stages {
        stage('Build') {
            when {
                branch 'main'
            }
            steps {
                echo 'Building on main branch...'
                // Add real build commands here (e.g., mvn package)
            }
        }
        stage('Test') {
            steps {
                echo 'Testing on any branch...'
                // Add your test commands here
            }
        }
        stage('Quality Scan') {
            when {
                branch 'main'
            }
            steps {
                echo 'Running quality checks only on main branch...'
                // Add your scan/SonarQube/static analysis steps here
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
    }
}
