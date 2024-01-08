@Library("jenkins-shared-library@main") _

pipeline {
    agent any
    stages {
        stage("hello") {
            steps {
                script {
                    hello.world()
                }
            }
        }
        stage("global variable") {
            steps {
                script {
                    echo(author.name())
                    echo(author.channel())
                }
            }
        }
    }
}