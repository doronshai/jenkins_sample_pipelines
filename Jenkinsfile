#!/usr/bin/env groovy

@Library('tikal-advanced-pipeline@master') _

pipeline 
{
    agent any
    stages 
    {
        stage('Code Update') 
        {
            steps 
            {
                echo "===================== 0.0 ========================"
            }
        }
    }
    post {
        success {
            sh 'echo 1111'
            notifyBuild('SUCCESS', '${WORKSPACE}\\sample.html')
            sh 'echo 2222'
        }
        failure {
            notifyBuild('FAILURE', '${WORKSPACE}\\sample.html')
        }  
        unstable {
            notifyBuild('UNSTABLE', '${WORKSPACE}\\sample.html')
        }            
    }
}
