pipeline{
    agent{
        label "nodejs"
    }
    stages{
        stage("Install dependencies"){
            steps{
               echo "Install all dependencies"
            }
        }

        stage("Check Style"){
            steps{
                echo "check style"
            }
        }

        stage("Test"){
            steps{
                echo "test"
            }
        }

        // Add the "Deploy" stage here
      stage("deployment") {
         steps {
         sh ''' 
         oc project hsaid-greetings
         oc start-build bc/greeting-service --follow --wait
         '''
         }
       }
     
    }
}
