pipeline {
    agent any

    stages {
         stage("Build"){
            agent{
                docker{
                    image 'node:18-alpine3.20'
                    reuseNode true
                }
            }
            steps{
                sh '''
                    ls -ls
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
    
    }
}
}