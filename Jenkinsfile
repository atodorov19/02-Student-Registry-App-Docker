pipeline{
    agent any
//Adding a comment
    
    stages{
        stage("Install NPM dependencies"){
            steps{
                bat 'npm install'
            }
        }    
        stage("Run Unit Tests"){
            parallel{
                stage("Unit Test 1"){
                    steps{
                        bat 'npm test'
                    }
                }
            }
                stage("Unit Test 2"){
                    steps{
                        bat 'npm test'
                    }
                }
            }
            steps{
                bat 'npm test'
            }
        }
        stage("Run Integration tests"){
            steps{
                echo "Running integration tests"
            }
        }
        stage("Deploy to production"){
            steps{
                input message: 'Deploy to production?', 
                    ok: 'Deploy'
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying application..."
            }
        }
    }

