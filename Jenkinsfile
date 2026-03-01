pipeline{
    agent any
    tools {
        maven "gk"
    }
    stages{
        stage("cloning the code"){
            steps{
            git branch: 'main', url: 'https://github.com/3gaurav/simple-java-app.git'
        }
    }
    stage("build application"){
            steps{
                echo "building the code"
            sh "mvn clean install"
        }
    }
    stage("artifacts"){
            steps{
                echo "packaging the code"
           archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
        }
    }
}
}
