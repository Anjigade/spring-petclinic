node ('OPENJDK-11-MVN')
{

   stage('SCM') {
      // git clone
	  git 'https://github.com/Anjigade/spring-framework-petclinic.git'
   }
   
   stage ('build the packages') {
      // mvn package
	  sh 'mvn package'
   }
      stage('Archive JUnit formatted test results') {
            steps {
                junit '**/surefire-reports/*.xml'
            }
        }
        stage('Archive artifacts') {
            steps {
            archive '**/target/*.jar'
            }
        }
   
   
}