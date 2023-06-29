pipeline {
    parameters{
        string(name:"EmailTo",defaultValue:'gk@gmail.com')
    }
    
    agent any

    tools{
        maven 'Maven'
    }
    stages {
        stage('Simple_print ') {
            steps {
                echo 'Hello World'
                sh "mvn --version"
               //bat 'cal'
            }
        }
        stage('Input_message') {
            
              
            input{
                    message "Continue?"
                    ok "please"
            }
            
            steps {
                echo 'test'
                //bat  echo '"$(BUILD_ID)"'
                }
               
            }
          
        
        stage('parameter_val') {
            steps {
                echo 'Hello Test'
                echo "${params.EmailTo}"
            }
        }
        stage('GK') {
            steps {
                echo 'Hello GK'
            }
        }
    }
    
    post{
        always
        {
            echo "I am a postaction"
            bat 'cal'
        }
        failure
        {
            echo "I am a postaction failure"
        }
        success
        {
            echo "I am a postaction success"
        }
    }
}
