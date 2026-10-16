pipeline{
    agent any
//Adding a comment
    
    stages{
        stage("Install NPM dependencies"){
            steps{
                bat 'npm install'
            }
        }    
        stage("Run Tests"){
            steps{
                bat 'npm test'
            }
        }
        stage("Deploy to production"){
            steps{
                input message: 'Deploy to production?', 
                    ok: 'Deploy'
            }
        }
        stage("Deploy")
            steps{
                echo "Deploying application..."
                bat "npm run deploy"    
            }
        }
    }

