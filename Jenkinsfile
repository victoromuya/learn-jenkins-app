pipeline {
    agent any

    stages {
         stage("Build"){
            agent{
                docker{
                    image 'node:18-slim'
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