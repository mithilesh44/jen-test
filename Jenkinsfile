pipeline {

  agent any
 
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -gs %M2SETTINGS% -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          bat "mvn test"
      }
    }

     stage('Development') {
      
      steps {
           bat 'mvn -U -V -e -B -gs %M2SETTINGS%  -DskipTests -PQa -Dusername=mithilesh107 -Dpassword=Mith@12345678 -DmuleDeploy
              }
    }
  
  }
}