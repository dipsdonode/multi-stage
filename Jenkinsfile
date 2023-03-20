pipeline {
	agent {
			label{
					label "built-in"
					customWorkspace "/mnt/custom"
					}
			}
			stages{
					stage ("on master"){
							steps {
									sh "yum install httpd -y"
									sh "yum install maven -y"
							}
					}
					stage ("On jenkins-slave-1"){
						agent{
							label {
								label "Jenkins-Slave-1"
								customWorkspace "/mnt/Jenkins-1"
									}
						}
						steps {
								sh "sudo yum install maven -y"
								sh "sudo yum install tree -y"
						}
					}
					
					stage ("On Jenkins-Slave-2") {
						agent {
							label {
								label "Jenkins-Slave-2"
								customWorkspace "/mnt/Jenkins-2"
						}	
								}
						steps {
								sh "sudo yum install maven -y"
								sh "sudo yum install tree -y"
						}
					}
			}
		}
