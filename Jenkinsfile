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
            notifyBuild('SUCCESS')
        }
        failure {
            notifyBuild('FAILURE')
        }  
        unstable {
            notifyBuild('UNSTABLE')
        }            
    }
}
