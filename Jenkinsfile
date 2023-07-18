pipeline{
    agent any
      parameters{
                string (
                    name : "PERSON",
                    defaultValue : "Mohan",
                    description : "variable value from input"
                )
                }
           environment{
                //Global variables
                name = "Jagan from global variable"
                psw = "***"
                     }
    stages {
        stage("Build")
        {
            steps {
               echo "${name}"
                echo "${params.PERSON}"
                  }
        }
          
                         
            }
        
    
}
