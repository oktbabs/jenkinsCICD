pipeline {
    agent any
       stages
          {
         stage('One'){
                  steps {
                         echo " Hi, This is Timmy form LablAn Technlogies Limited !"

                         }
                     } 

         stage('Two'){
                  steps {
                         input("Do you want to proceed ?")

                         }
                     } 
         stage('Three'){
                  when {
                         not {
                               branch "master"
                             }

                         }
                        steps {
                               echo " Hello"
                              }
                     } 
         stage(Four'){
                  parallel {
                    stage('Unit Test'){
                                   steps{

                                          echo " Running the UNIT TEST !!! "
                                        }
                                      }
                    stage('Integration Test'){
                            agent {
                                    docker {
                                             reusenode false
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
