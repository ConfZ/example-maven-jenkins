pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
    post {
        success {
            bash <(curl -s https://scripts.scantist.com/ci-travis.sh)
        }
    }
}
