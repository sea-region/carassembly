pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'rm -rf build' //This is testing//
                sh 'mkdir build'
                sh 'touch build/car.txt'
                sh 'echo "chassic" > build/car.txt'
            }
        }
        
        stage('Test') {
            steps {
                sh 'test -f build/car.txt'
                sh 'grep "chassic" build/car.txt'
                
            }
        }
        
        stage('publish') {
            steps {
                 archiveArtifacts artifacts: 'build/'
            }
        
        }
    }
}
