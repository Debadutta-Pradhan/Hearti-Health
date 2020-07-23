pipeline {
    agent any
        stages {
            stage('package'){
                steps{
                    bat '''
                         npm install
                     '''
                    }
            }

                stage('npm start'){
                    steps{
                        bat '''
                            npm start  
                        '''
                    }
                }   
                stage('npm run'){
                    steps{
                        bat '''
                            npm run ng -- build --prod  
                        '''
                    }
                }
       }
}
