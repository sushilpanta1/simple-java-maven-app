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
            sh "mvn clean test surefire-report:report-only"
        }
    }
    stage('Packaging') {
        steps {
            sh "mvn package -Dskiptests=true"
        }
        post {
            success {
                echo "Inside Packaging stage - Success"
            }
            always {
            echo "Inside Packaging stage - Always"
            }
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





