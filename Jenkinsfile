pipeline{
    agent any
    environment {
        DEPLOY_TO = "Prods"
    }
    stages{
        stage('Deploy to main')
        {
        when{
            branch 'main'           
            }
        steps{            
            echo "Deploy into main branch"
        }
        }
        stage("Deploy to Prod")
        {
            when{
                anyOf {
                expression{BRANCH_NAME ==~ /(Prod|mains)/}
                 environment (name : DEPLOY_TO,value : 'Prod')
                }
                }
            steps{           
            echo "Deploy into prod branch"
            }
        }
        stage('tag deployment')
        {
           // when {
               // buildingTag()
              // tag pattern : "v\\d{1,2}.\\d{1,2}.\\d{1,2}"
            //}
            steps {
                echo "${TAG_NAME}"
                echo "deploying tag"
            }
        }
        }
    
}
