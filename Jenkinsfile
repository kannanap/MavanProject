node{

   stage('SCM CHECKOUT'){

      println ".................Code Checkin and Checkout...................."

     git credentialsId: '94e6862e-a136-4850-b3e3-e167852a1cdb', url: 'https://github.com/kannanap/JaveProject.git'

   }

   stage('COMPILE AND PACKAGING'){

      // Get maven home path

      println ".................Maven Compile and Packaging...................."

      def mvnHome = tool name: 'Maven_3_5_3', type: 'maven'

      def mvnCMD  = "${mvnHome}/bin/mvn"

      sh "${mvnCMD} clean package"

       
  post {
        success {
            mail to:"kannanoradba@gmail.com", subject:"SUCCESS: ${currentBuild.fullDisplayName}", body: "Build Job is SUCCESSFULL, we passed."
        }
        failure {
            mail to:"someone@hotmail.com", subject:"FAILURE: ${currentBuild.fullDisplayName}", body: "Build Job Failed see the logs, we failed."
        }
    }   
}  
} 

}

    
      
   
