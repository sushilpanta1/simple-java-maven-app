node('docker'){
    stage('checkout'){
        echo "Checking the Git code"
        //git brach: 'docker' credentialsId: 'lokigithubapikey', url: 'https://github.com/lokeshkamalay/simple-java-maven-app.git'
        checkout scm
    }
    stage('Executing Test Cases'){
        docker.image('lokeshkamalay/batch2:maven').inside(){
            echo "Execuring Test Cases Started"
            sh "mvn clean deploy --settings settings.xml"
        }
    }
}
