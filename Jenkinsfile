pipeline{
    agent any
    tools {nodejs "20.4.0"}
    stages {
   /*     stage('checkout'){
            steps{
                git branch: 'main',
                    url: 'https://github.com/nalinture/nodejs_app.git'
            }
        } */
        
        stage('Build'){
            steps {
                sh 'npm install'
            }
        }
         stage('Build pm2'){
            steps {
                sh 'npm install pm2 -g'
            }
        }
        
        stage('Deploy'){
            steps {
                sh 'pm2 startOrRestart pm2.config.json'
            }
        }
    }
}
