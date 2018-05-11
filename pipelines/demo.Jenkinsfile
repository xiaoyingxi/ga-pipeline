@Library("pipeline-library") _

properties([parameters([string(defaultValue: 'dev', description: 'the remote branch or commit hash to be released', name: 'commit')])])

microServicePipeline(
	build: 'javaMicroServiceRelease', 
	imageName: 'yuuyoo/demo',
    repoUrl: 'git@github.com:xiaoyingxi/spring-boot-demo.git',
    credentialsId: 'b4eb337d-e113-45d0-800e-67c072a4926b', 
    branch: 'master', 
    serviceName: 'yuuyoo-demo', 
    commit: "${params.commit}",
    runner: 'ProjectDirectory/MicroService/MicroserviceRunner'
)
