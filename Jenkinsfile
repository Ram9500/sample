pipeline{
    agent any
    environment{
        PATH = "/opt/apache-maven-3.8.2/bin:$PATH"
    }
    stages{
        stage('Git checkout'){
            steps{
               git credentialsId: 'github', url: 'https://github.com/Ram9500/sample.git'
            }
        }
        stage('Maven Build'){
          steps{
		  step{
			  def mvnHome =  tool name: 'maven3', type: 'maven'   
               sh "${mvnHome}/bin/mvn clean package"
	           sh 'mv target/myweb*.war target/newapp.war'
		  }
          }   
        }
    }
}
