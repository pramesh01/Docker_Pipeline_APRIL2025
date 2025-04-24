pipeline{
    agent any
    stages{
<<<<<<< HEAD
        stage('building jar'){
            steps{
                bat "mvn clean package -DskipTests"
=======
        stage('Bring Grid UP'){
            steps{
                bat "docker-compose -f grid.yaml up -d"
>>>>>>> 691298b (pushing new sets of Files Updated)
            }

        }

<<<<<<< HEAD
        stage('build image'){
            steps{
                bat "docker build -t=pramesh11/myprojectimage_april25:latest ."
            }


        }
        stage('push image'){
            environment{
                DOCKER_HUB=credentials('dockerhub-credentials')
            }
            steps{
              bat "docker login -u %DOCKER_HUB_USR% -p %DOCKER_HUB_PSW%"
              bat "docker push pramesh11/myprojectimage_april25:latest"
              bat "docker tag pramesh11/myprojectimage_april25:latest pramesh11/myprojectimage_april25:${env.BUILD_NUMBER}"
              bat "docker push pramesh11/myprojectimage_april25:${env.BUILD_NUMBER}"

            }
        
        }

    }
=======
        stage('Running Tests'){
            steps{
                bat "docker-compose -f test_suite.yaml up"
            }

        }
      

    }
   post{
     always{
        bat "docker-compose -f grid.yaml down"
        bat "docker-compose -f test_suite.yaml down"
     }
   } 
>>>>>>> 691298b (pushing new sets of Files Updated)
   
}