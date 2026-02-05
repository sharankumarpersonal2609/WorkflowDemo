pipeline{
agent any
stages{
stage('Checkout'){
steps{
git 
}
}
stage('Dockerbuild'){
steps{
sh 'docker build -t demo .'
}
}
stage('DockerContainer'){
steps{
sh 'docker run -d -p 8000:80 demo'
}
}
}
}
