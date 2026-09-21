pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                echo "Building Started"
                deleteDir()
                sh '''
                    git clone https://github.com/shifna8547/genkins.git
                    ls -l
                '''
            }
        }
        stage('deploy'){
            steps{
                echo "Deployment Started"
                sh '''
                    rm -rf /var/www/html/*
                    cp -r genkins/* /var/www/html
                    ls -l /var/www/html
                '''
            }
        }
    }
}
