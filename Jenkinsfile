pipeline
{
	agent none
	stages
	{
		stage("stage01")
		{
			agent
			{
				docker
				{
					 image "maven:3-alpine"
                                	 label "dockerslave"
				}
			}
			steps
			{
				echo "Hello maven"
				sh "mvn --version"
			}
		}
		stage("stage02")
		{
			agent
                        {
                                docker
                                {
                                         image "openjdk:8-jre"
                                         label "dockerslave"
                                }
                        }
			steps
                        {
                                echo "Hello Java"
                                sh "java --version"
                        }
		}
	}
}
