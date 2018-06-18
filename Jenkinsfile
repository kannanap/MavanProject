node {
  stage('SCM CheckOut')
  {
      //git 'https://github.com/kannanap/MavanProject.git'
    git credentialsId: '94e6862e-a136-4850-b3e3-e167852a1cdb', url: 'https://github.com/kannanap/MavanProject.git'
  }
  //stage ('Compile-Package')
  //{
   // def mvnHome =  tool name: 'Maven_3_5_3', type: 'maven'    
    // sh "${mvnHome}/bin/mvn clean package"  
  //}
  stage('Mvn Package') {
  sh 'mvn clean package'
  }
  

}

    
      
   
