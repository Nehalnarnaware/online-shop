node{

    stage('SCM Checkout')
    {
        git credentialsId: 'GIT_HUB_CREDENTIALS', url: 'https://github.com/Nehalnarnaware/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker version'
        sh 'docker build -t jhooq-docker-demo .'
        sh 'docker image list'
        sh 'docker tag jhooq-docker-demo snehalnar/nehal2:jhooq-docker-demo'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "nehalnar" -p "Nehal@123" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push nehalnar/global'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}

