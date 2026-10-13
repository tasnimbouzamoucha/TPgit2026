pipeline {
    agent any
    tools {
        jdk 'JDK21'
    }
    stages {
        stage('Echo') {
            steps {
                echo 'Début du pipeline CI pour TPgit2026'
            }
        }
        stage('Checkout code') {
            steps {
                git branch: 'master', url: 'https://github.com/tasnimbouzamoucha/TPgit2026.git'
            }
        }
        stage('Compile code') {
            steps {
                sh 'cd src && javac application/test.java'
            }
        }
        stage('Execute code') {
            steps {
                sh 'cd src && java application.test'
            }
        }
    }
}
