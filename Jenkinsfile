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
        stage("resource compile") {
            steps {
                script {
                    def config = libraryResource("config/build.json")
                    echo(config)
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