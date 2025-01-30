pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                echo "let's see the files"
                sh "ls"
                echo "let's create a new script"
                mkdir newfolder
                sh touch newscript.sh
                echo "echo 'I'm a new script!" > newscript.sh
            }
        }
        stage('Test){
            steps {
                sh newscript.sh
                mv newscript.sh $pwd/newfolder
                echo "echo 'I've been moved!" >> $pwd/newfolder/newscript.sh
            }
          }
