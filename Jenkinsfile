pipeline{
    agent any
    stages {
        stage("Build")
        {
            environment{
                //Global variables
                name = "Jagan from global variable"
                psw = "***"
            }
            parameters{
                string (
                    name : "name",
                    defaultValue : "Mohan"
                    discription : "variable value from input"
                )
                echo "${name}"
                echo "${params.name}"                
            }
        }
    }
}
