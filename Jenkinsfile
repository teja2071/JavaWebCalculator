pipeline{
    
     tools{
        jdk 'myjava'
        maven 'mymaven'
    }
    agent {label 'pipeline_slave'}
    stages{
        stage('checkout'){
            steps{
               git 'https://github.com/teja2071/JavaWebCalculator.git'
            }
        }
         stage('Compile'){
              
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('UnitTest'){
               
              steps{
                  sh 'mvn test'
               }
           }	
          }
          stage('Package'){
        
              steps{
                  sh 'mvn package'
              }
          }
}
