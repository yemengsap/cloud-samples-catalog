#!/usr/bin/env groovy

@Library('piper-library-os-experimental') _

stage ('mta') {
    node {
	deleteDir()
	checkout scm
        setupCommonPipelineEnvironment script: this
	mtaBuild script: this, dockerImage: 'yemengsap/mta:latest', buildTarget: 'CF'
    }
}
stage('cf deploy') {
    node {
        cloudFoundryDeploy script: this, deployTool: 'mtaDeployPlugin', mtaPath: 'cloud.samples.catalog.mtar'
    }
}
