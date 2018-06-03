@Library("pipeline-library") _

properties([parameters([
    string(name: 'targetRepo', defaultValue: 'https://nexus.yuuyoo.com/repository/maven-releases/', description: 'the target location of published repo'),
    string(name: 'version', description: 'the version of current release, such as 1.0.0, 2.0.0'),
    string(name: 'newVersion', description: 'the new version for next iteration'),
    choice(name: 'branch', description: 'the release on target branch',
        choices: 'master\
                 ')
    ])])

javaLibraryPipeline(
    version: "${params.version}",
    newVersion: "${params.newVersion}",
    targetRepo: "${params.targetRepo}",
    branch: "${params.branch.trim()}",
    credentialsId: "6f229e8b-c982-4ca4-97d3-2edac7bc8df8",
    repoUrl: 'git@github.com:xiaoyingxi/spring-boot-starter-logging.git',
    description: "spring-boot-starter-logging:${params.version}" 
)
