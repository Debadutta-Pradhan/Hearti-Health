pipeline {
    agent any
        stages {
            stage('NPM SetUp'){
                steps{
                    bat '''
                         npm install
                     '''
                    }
            }

                stage('Build'){
                    steps{
                        bat '''
                            npm run build  
                        '''
                    }
                }
                stage('Stage Web Build'){
                    steps{
                        bat '''
                            npm run ng build --prod  
                        '''
                    }
                }

                stage('Deploy'){
                    steps{
                        bat '''
                            pm2 restart all  
                        '''
                    }
                }
        }
}
