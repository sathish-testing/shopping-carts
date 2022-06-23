pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    

    stages{
        stage('compile'){
            steps{
                echo 'this is the first job'
                sh 'mvn compile'
                
            }
        }
        stage('test'){
            steps{
                echo 'this is the second job'
                sh 'mvn test'
                
            }
        }
        stage('package'){
            steps{
                echo 'this is the third job'
                sh 'mvn package -DskiptTests'
                
            }
        }
    }
    
    post{
        always{
            echo 'this is my first pipeline has completed...'
        }
        
    }
    
}


