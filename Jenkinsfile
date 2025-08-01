// pipeline {
//    agent any
//    stages {
//      stage('BUILD') {
//        steps {
//          echo "This is Build Stage"
//        }
//      }
//        stage('DEPLOY') {
//        steps {
//          echo "This is DEPLOY Stage"
//        }
//      }
//        stage('TEST') {
//        steps {
//          echo "This is TEST Stage"
//        }
//      }
//    } 
// }
pipeline {
   agent any
    stages {
		stage('BUILD') {
			steps {
			 echo "This is Build Stage"
            }
        }
		
        stage('DEPLOY') {
		    parallel {
			    stage('SERVER 1') {
					steps {
                     echo "This is Deploy to server 1"
				    }
		        }
				
				stage('SERVER 2') {
					steps {
                     echo "This is Deploy to server 2"
				    }
		        }
				
				 stage('SERVER 3') {
					steps {
                     echo "This is Deploy to server 3"
				    }
		        }
            }
        }
		
        stage('TEST PARALLEL') {
	        parallel{
				stage(TEST ON CHROME) { 
					steps {
					  echo "This is TEST on Chrome browser"
		              
		                    } 
                        }
				
				stage(TEST ON SAFARI) { 
					steps {
					  echo "This is TEST on Safari browser"
		              
		                    } 
                         }
	        }
           }
     }
} 
