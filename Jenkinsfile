node {
  stage('SCM CheckOut')
  {
      git 'https://github.com/kannanap/MavanProject.git'
  }
  stage ('Compile-Package')
  {
    def mvnHome =  tool name: 'Maven_3_5_3', type: 'maven'    
     sh "${mvnHome}/bin/mvn package"  
  }
}
    
      
   
