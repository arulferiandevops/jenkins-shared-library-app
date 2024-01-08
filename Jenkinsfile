@Library("jenkins-shared-library@main") _

pipeline {
    agent any
    stages {
        stage("maven compile") {
            steps {
                script {
                    maven(["clean","compile","test"])
                }
            }
        }
        stage("person") {
            steps {
                script {
                    person.person([
                        firstName: "arul",
                        lastName: "a"
                    ])
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