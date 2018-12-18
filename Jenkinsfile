#!/usr/bin/env groovy

@Library('piper-library-os-experimental') _

stage ('first stage') {
    node {
        echo "Hello world!"
	mtaBuild script:this, mtaJarLocation:'..', buildTarget:'CF'
    }
}
