pipeline {
    agent { label "agent-crud" }
  
    stages {
        stage("Code Clone") {
            steps {
               echo "Cloning The Repo"
               git url: 'https://github.com/Sat70/Deployment-Crud-Mean-App.git', branch: 'main'
               echo "Cloned Successfully"
            }
        }

        stage("Build Docker Images") {
            steps {
                script {
                    echo "Building"
                    sh "docker-compose up -d"
                    echo "Build Successfully"
                }
            }
        }

        stage("Push to DockerHub"){
            steps{
                 echo "This is pushing the image to Docker Hub" 
                 withCredentials([usernamePassword("credentialsId': "dockerHubCred" 
                 passwordVariable: "dockerHubPass" 
                 usernameVariable: "dockerHubUser"}]){
                 "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPass}"
                 sh "docker image tag notes-app:latest ${env. dockerHubUser)/crud-app:latest"
                 sh "docker push ${env.dockerHubUser}/crud-app:latest"
                 }
            }
        }
        stage("Deploy"){
            steps{
                deploy()
            }
        }
    }
}
