node{

    stage('SCM Checkout')
    {
     git url: 'https://github.com/Nehalnarnaware/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
 
}
