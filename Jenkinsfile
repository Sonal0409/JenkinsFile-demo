pipeline{
    agent none
    tools{
        maven 'mymaven'
    }
    stages{
        stage('clone Repo'){
            agent{
                label 'linux_node'
            }
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('CompileCode'){
            agent any  // run on master node
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
                sh 'mvn compile'
            }
        }
         stage('ReviewCode'){
             agent any
            steps{
                sh 'mvn pmd:pmd'
            }
        }
         stage('TestCode'){
             agent{
                 label 'linux_node'
             }
            steps{
                sh 'mvn test'
            }
        }
         stage('BuildCode'){
              agent{
                 label 'linux_node'
             }
            steps{
                sh 'mvn package'
            }
        }
    }
}
