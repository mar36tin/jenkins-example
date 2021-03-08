pipeline {
    agent { 
        docker { 
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2'
        } 
    }
    stages {
        stage('Version') {
            steps {
                sh 'mvn --version'
                echo 'Building..'
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
    
}

