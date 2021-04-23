pipeline {
agent none
stages {

stage ('Non-parallel Stage'){
agent {
label 'master'
}
steps {
echo 'This will get executed first for checkout git code or deployment'}
}
   
stage('Run Test'){
   parallel { //PARALLEL keyword used for mentioning the stages below to be run parallely
stage ('TEST ON WINDOWS')
{
agent { label 'Windows_Node1'
}
steps 
{echo "TASK 1 ON WINDOWS NODE1";
}
}
stage('TEST ON MASTER')
{
agent 
{ label 'master'
}
steps
{echo "TASK 2 ON MASTER AGENT !!!";
}
}

}
}
}
}
