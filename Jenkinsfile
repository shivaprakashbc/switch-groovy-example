pipeline {
    
    agent any
    
    parameters {
           string defaultValue: '\'image1\',\'image2\',\'image3\',\'image3a\',\'image3b\',\'image4\'', description: 'Docker Image to test', name: 'IMAGE'
           string defaultValue: '\'image3a\',\'image3b\'', description: 'Docker Sub-Images to test', name: 'IMAGE_SUB'
           choice choices: ['Dev', 'Prod', 'QA'], name: 'ENV'
               }
    
    stages {
        stage("Testing for image1") {
            when{
                        expression {params.IMAGE == "image1"}
                }
            steps {
                script {
                    switch(params.ENV) {
                        case "Dev": echo "image1 testing in dev"; break
                        case "Prod": echo "image1 testing in Prod"; break
                        case "QA": echo "image1 testing in QA"; break
                    }
                }
            }
        }
        stage("Testing for image2") {
            when{
                        expression {params.IMAGE == "image2"}
                }
            steps {
                script {
                    switch(params.ENV) {
                        case "Dev": echo "image2 testing in dev"; break
                        case "Prod": echo "image2 testing in Prod"; break
                        case "QA": echo "image2 testing in QA"; break
                    }
                }
            }
        }
        stage("Testing for image3") {
            when{
                        expression {params.IMAGE == "image3"}
                }
                stages{
                    stage('Testing for image3a'){
                       when{
                        expression {params.IMAGE_SUB == "image3a"}
                        }
                       steps {
                           script {
                                switch(params.ENV) {
                                    case "Dev": echo "image3a testing in dev"; break
                                    case "Prod": echo "image3a testing in Prod"; break
                                    case "QA": echo "image3a testing in QA"; break
                                }
                            }
                        }
                    }
                    stage('Testing for image3b'){
                       when{
                        expression {params.IMAGE_SUB == "image3b"}
                        }
                       steps {
                           script {
                                switch(params.ENV) {
                                    case "Dev": echo "image3b testing in dev"; break
                                    case "Prod": echo "image3b testing in Prod"; break
                                    case "QA": echo "image3b testing in QA"; break
                                }
                            }
                        }
                    }
                }
            }
        stage("Testing for image3a") {
            when{
                        expression {params.IMAGE == "image3a"}
                }
            steps {
                script {
                    switch(params.ENV) {
                        case "Dev": echo "image3a testing in dev"; break
                        case "Prod": echo "image3a  testing in Prod"; break
                        case "QA": echo "image3a testing in QA"; break
                    }
                }
            }
        }
        stage("Testing for image3b") {
            when{
                        expression {params.IMAGE == "image3b"}
                }
            steps {
                script {
                    switch(params.ENV) {
                        case "Dev": echo "image3b testing in dev"; break
                        case "Prod": echo "image3b testing in Prod"; break
                        case "QA": echo "image3b testing in QA"; break
                    }
                }
            }
        }
        stage("Testing for image4") {
            when{
                        expression {params.IMAGE == "image4"}
                }
            steps {
                script {
                    switch(params.ENV) {
                        case "Dev": echo "image4 testing in dev"; break
                        case "Prod": echo "image4 testing in Prod"; break
                        case "QA": echo "image4 testing in QA"; break
                    }
                }
            }
        }
    }
}
