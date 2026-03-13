@Library("shared") _ 

pipeline {
    agent {label "mac"}
    stages {
    
    stage('hello') {
        steps{
            script{
                hello()
            }
        }
    }
    
    stage('code') {
        steps {
            script{
                code()
            }
        }
    }

    stage('build') {
        steps {
            script{
                build()
            }
        }
    }

    stage('push to docker repo') {
        steps {
            push_hub()
        }
    }

    stage('deploy') {
        steps {
            deploy()
        }
    }

}
}
