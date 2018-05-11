@Library("pipeline-library") _

properties([parameters([string(defaultValue: 'dev', description: 'the remote branch or commit hash to be released', name: 'commit')])])

microServicePipeline(
	build: 'javaMicroServiceRelease', 
	imageName: 'yuuyoo/demo',
    repoUrl: 'git@github.com:xiaoyingxi/spring-boot-demo.git',
    credentialsId: '9daced0c-e897-4c39-86d7-c6834e490ab4', 
    branch: 'master', 
    serviceName: 'yuuyoo-demo', 
    commit: "${params.commit}",
    runner: 'ProjectDirectory/MicroService/MicroserviceRunner'
)
