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
    
 
}
   post {
        failure {
            mail to: 'kannanoradba@gmail.com', from: 'kannanoradba@gmail.com',
                subject: "Example Build: ${env.JOB_NAME} - Failed", 
                body: "Job Failed - \"${env.JOB_NAME}\" build: ${env.BUILD_NUMBER}\n\nView the log at:\n ${env.BUILD_URL}\n\nKannan's Job Executions:\n${env.RUN_DISPLAY_URL}"
        }
    }
}
} 

}

    
      
   
