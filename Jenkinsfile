@Library("jenkins-shared-library@main") _

pipeline {
    agent any
    stages {
        stage("maven") {
            steps {
                script {
                    maven("clean compile")
                }
            }
        }
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
                    echo(author())
                    echo(author.channel())
                }
            }
        }
    }
}