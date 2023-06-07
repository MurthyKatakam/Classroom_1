pipeline {
    agent any
    parameters {
        //  choice(name: 'CHOICE', choices: ['DEV', 'STAGE', 'PROD'], description: 'Pick Environment')
    }
   
    stages {
        stage('Hello') {
            when {
                    expression {params.CHOICE == 'DEV'}
            }
            steps {
                input('Do you want to proceed?')
                echo 'Hello World DEV'
                
            }
        }
        stage('build'){
             when {
                    expression {params.CHOICE == 'DEV'}
            }
            stages {
                stage ( 'stsges in stsge 1') {
                    steps {
                        // sh "mkdir test"
                        // sh "touch ./test/tet.txt"
                        sh " echo ${params.CHOICE} > ./test/tet.txt"
                        // def exixts = fileExists 'tet.txt'
                        script{
                        if (fileExists ('./test/tet.txt') ) {
                            sh "rm ./test/tet.txt "
                            
                        } else {
                            sh "echo dont exuixsts"
                        }
                        }
                    }
                }
                 stage ( 'stsges in stsge 2') {
                    steps {
                     echo "in ${params.CHOICE}"
                    }
                }
                 stage ( 'stsges in stsge 3') {
                    steps {
                     echo "in ${params.CHOICE}"
                    }
                }
            }
        }
        stage('Hele4rlo') {
            steps {
                echo 'Hello World'
            }
        }
        stage('builqwerd'){
             when {
                    expression {params.CHOICE == 'STAGE'}
            }
            stages {
                stage ( 'stsges in stsge 1') {
                    steps {
                    echo "in ${params.CHOICE}"
                    }
                }
                 stage ( 'stsges in stsge 2') {
                    steps {
                     echo "in ${params.CHOICE}"
                    }
                }
                 stage ( 'stsges in stsge 3') {
                    steps {
                     echo "in ${params.CHOICE}"
                    }
                }
            }
        }
        
    }
}
