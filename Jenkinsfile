pipeline{
agent any{
stages{
stage('Checkout'){
steps{
git 
}
}
stage('Dockerbuild'){
steps{
sh 'Docker build -t demo .'
}
}
stage('DockerContainer'){
steps{
sh 'Docker run -d -p 8000:80 demo'
}
}
}
}
