pipeline {
agent any

stages {

stage('Checkout from GitHub') {
steps {
git branch: 'main', url: 'https://github.com/sazia7398/static-lab1-docker-github.git'
}
}

stage('Build Docker Image') {
steps {
bat 'docker build -t static-site:67 .'
}
}

stage('Run Container') {
steps {
bat 'docker run -d -p 5600:80 --sweety static-site:67'
}
}
}
}
