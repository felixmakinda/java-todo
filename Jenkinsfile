pipeline{
    agent any
    tools{
        gradle "Gradle-6"
    }
    stages{
        stage ('Clone Code'){
            steps{
            git branch:'master', url:'https://github.com/felixmakinda/java-todo.git'
            }
        }
        stage ('Build Code'){
            steps{
                sh 'gradle build'
            }
        }
        stage ("Test Code"){
            steps {
                sh 'gradle test'
            }
        }
    }
}