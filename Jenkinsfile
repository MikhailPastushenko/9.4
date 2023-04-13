pipeline{
    agent{
       label 'linux'
    }
    stages{
        stage('git'){
            steps{
                sh 'rm -rf *.*'
                sh 'git clone https://github.com/MikhailPastushenko/ansible8.4.git'
                sh 'cd ansible8.4'
                dir('roles'){
                    sh 'pwd'
                }
                dir('clickhouse-role'){
                    sh 'pwd'
                }
            }
        }
        stage('molecule'){
            steps{
                sh 'molecule test'
            }
        }
            
    }
}
