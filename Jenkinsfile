properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/jasondbaker/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
            },
    stage ("GetInstances") {
        sh "aws ec2 describe-instances --region us-east-1"
            },
    stage ("CreateInstance") {
        sh "aws ec2 run-instances --image-id ami-06b382aba6c5a4f2c --count 1 --instance-type t2.micro 
        --key-name SEIS665022019 --security-group-ids SEIS665022019 --subnet-id subnet-076da1922f68a49a2 --region us-east-1"

}        
            
}
