node {
         stage ('Checkout SCM'){
                    git branch: 'master',url: 'https://github.com/La-litha/Hearti-Health.git'
         }
         
         stage('Install node modules'){
                      sh "npm install"
         }
         stage('Build'){
                     sh "npm run ng -- build --prod"
         }
         stage('Deploy'){
                      sh "pm2 restart all"
         }
     }
