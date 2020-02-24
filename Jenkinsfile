pipeline {
    agent {
        label 'maven'
    }
    tools {
        jdk 'Openjdk8'
        maven 'maven363'
}
stages {
    stage('Test') {
        steps {
            sh "mvn clean test"
        }
    }
}
post {
    success {
        echo "Good Job"
    }
    failure {
        echo "Improve the skills"
    }
    always {
        echo "Work Hard"
        }
    }
}





