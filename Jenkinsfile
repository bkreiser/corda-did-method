pipeline {

    options {
        gitLabConnection("GitLab_corda_did_method")
    }

    agent {
        docker {
            image 'gradle:jdk8-slim'
            args '-v /root/book_management:/home/gradle/.gradle'

        }
    }

    stages {

        stage('clean') {
            steps {
                sh "./gradlew clean"
            }

        }
        stage('build') {

            steps {

                sh "./gradlew build"
            }
        }
    }
}