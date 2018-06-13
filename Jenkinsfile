pipeline 
{
 agent any 
	  stages 
	{
   		stage ('Compile Stage') 
		{
		steps 
		  {
		withMaven(maven : 'Maven_3_5_3')
			{
			sh 'mvn clean compile'
			}
     		  }		
   		}
   		stage ('Testting Stage')
		 {
		steps 
		    {
		     withMaven(maven : 'Maven_3_5_3') 
		      {
		     sh 'mvn test'
		      }
      		     }
		  }
		stage ('Deployment Stage') 
		{
		steps 
		   {
	           withMaven(maven : 'Maven_3_5_3')
		   	{
	           	sh 'mvn deploy'
	           	}
                   }
                 }
	}
}
