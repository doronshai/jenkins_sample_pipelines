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
            notifyBuild('SUCCESS', '${WORKSPACE}\sample.html')
        }
        failure {
            notifyBuild('FAILURE', '${WORKSPACE}\sample.html')
        }  
        unstable {
            notifyBuild('UNSTABLE', '${WORKSPACE}\sample.html')
        }            
    }
}
