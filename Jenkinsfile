pipeline { 
    agent { label 'slave2' } 
    stages { 
        stage ('Checkout') { 
            steps {
                sh "pwd"
                sh "rm -rf hello-world-war"
                sh "git clone https://github.com/Sahanamahadev29/hello-world-war.git"
            }
        }
        stage ('Build') { 
             steps {
              sh "ls"
              sh "cd"
              sh "mvn clean package"
             }
        }
        stage ('Deploy') { 
             steps {
               sh "cp -r /home/slave2/workspace/helloworld_project/target/hello-world-war-1.0.0 /opt/tomcat/webapps"
             }
        }
    }           
 }
