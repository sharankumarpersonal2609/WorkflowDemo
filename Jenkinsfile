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
sh 'docker build -t sharan2609/demo:1.0 .'
}
}
stage('Dockerpush'){
steps{
sh 'docker push sharan2609/demo:1.0'
}
}
stage('DockerContainer'){
steps{
sh '''
docker rm -f demo_container || true
docker run -d --name "demo_container" -p 8000:80 sharan2609/demo:1.0
'''
}
}
}
}
