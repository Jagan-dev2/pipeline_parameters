pipeline{
    agent any
    environment {
        DEPLOY_TO : "Prod"
    }
    stages{
        stage('Deploy to main')
        {
        when(branch 'main')
        steps{            
            echo "Deploy into main branch"
        }
        }
        stage("Deploy to Prod")
        {
            when(branch 'Prod')
            steps{           
            echo "Deploy into main branch"
        }
        }
    }
}
