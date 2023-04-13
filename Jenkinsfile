pipeline {

    agent any
    environment {
        PASSWORD_DB = credentials('PASSWORD_DB')


    }

    parameters {


        choice(name: 'APPLICATION', choices: ['python', 'java'], description: 'Application to work')
    }

    stages {


        stage("build"){

            stages {

            stage("build python"){
                when {
                    expression {
                        params.APPLICATION = 'python'
                    }
                }

                steps { 
                    
                    echo 'Build python'
                }

            }

            stage("build java"){
                when {
                    expression {
                        params.APPLICATION = 'java'
                    }
                }

                steps {
                    echo 'Build python'

                }

            }

            }


        }

        stage("test"){

            steps{

                echo 'test'
                
            }

            

        }

        stage("deploy"){

        steps{

                echo 'test'
                
            }
        }


    }



}