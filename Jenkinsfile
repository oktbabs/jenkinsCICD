pipeline {
    agent any
       stages
          {
         stage('One'){
                  steps {
                         echo " Hi, This is Timmy form Lablan Technlogies Limited !"

                         }
                     }

         stage('Two'){
                  steps {
                         input("Do you want to proceed now ?")

                         }
                     }
         stage('Three'){
                  when {
                         not {
                               branch "master"
                             }

                         }
                        steps {
                               echo " Hello Timmy, man"
                              }
                     }
         stage('Four'){
                  parallel {
                    stage('Unit Test'){
                                   steps{

                                          echo " Running the UNIT TEST START !!! "
                                        }
                                      }
                    stage('Integration Test'){
                            agent {
                                    docker {
                                             reuseNode true	
                                             image 'ubuntu'
                                           }
                                    }
                                   steps{

                                          echo " Running the INTEGRATION TEST !!! "
                                        }
                                      }
                           }
                    }


         }
}
                                                                               
