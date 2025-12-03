pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Building Image..'
                bat 'docker build -t exam_app .'
            }
        }
        stage('Run'){
            steps{
                bat 'docker rm -f mycontainer || exit 0'
                bat 'docker run -d -p 5000:5000 --name mycontainer exam_app'
            }
        }
    }
}