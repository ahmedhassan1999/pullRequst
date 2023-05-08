
pipeline 
{
        agent any
        tools 
        {
        terraform 'terraform'
        }
    stages 
    {

        
        stage('terraform format check') 
        {
            steps
            {

                sh 'terraform fmt'
            }
        }


        stage('terraform Init') 
        {
            steps
            {

                withAWS(region:'us-east-1') 
                {
                    withAWS(credentials:'iam') 
                    {
                          sh 'terraform init'
    
                    }
                    
    
                }
              
            }
        } 

        

       
    }
}
