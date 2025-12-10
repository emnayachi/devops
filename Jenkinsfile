pipeline {
    agent any
    
    tools {
        jdk 'JAVA_HOME'      // Doit correspondre au nom exact configuré dans Jenkins
        maven 'M2_HOME'      // Doit correspondre au nom exact configuré dans Jenkins
    }
    
    stages {
        stage('GIT') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/hwafa/timesheetproject.git'
            }
        }
        
        stage('Compile Stage') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}