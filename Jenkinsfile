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
                expression{BRANCH_NAME == /(Prod|mains)/}
                 environment (name : DEPLOY_TO,value : 'Prod')
                }
                }
            steps{           
            echo "Deploy into prod branch"
        }
        }
    }
}
