pipeline{
agent any
stages{
stage('Checkout'){
steps{
checkout scm
}
}
stage('Dockerbuild'){
steps{
sh 'docker build -t demo .'
}
}
stage('DockerContainer'){
steps{
sh '''
docker rm -f demo_container || true
docker run -d --name "demo_container" -p 8000:80 demo
'''
}
}
}
}
