pipeline {
    agent {
        label 'maven'
    }
    tools {
        jdk 'Openjdk8'
        maven 'maven363'
}
stages {
    stage('Build'){
        steps{
            sh "mvn clean test" //whats up
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





