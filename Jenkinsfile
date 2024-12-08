pipeline{
    agent any
    stages{
        stage('GitHub access'){
            steps{
                script{
                    echo 'Clonning github repository'
                    git 'https://github.com/bhavvzs/1.git'
                }
            }
        }
        stage('Java Program Execution'){
            steps{
                script{
                    echo 'compiling and executing java program'
                    bat 'javac Helloworld.java'
                    bat 'java Helloworld'
                }
            }
        }
        stage('Python Program Execution'){
            steps{
                script{
                    echo 'running python program'
                    bat 'python helloworld.py'
                }
            }
        }
    }
    post{
        always{
            echo 'Pipeline execution completed' 
        }
        success{
            echo 'Pipeline completed successlly'
        }
        failure{
            echo 'Pipeline failure.Check logs for details'
        }
    }
}
