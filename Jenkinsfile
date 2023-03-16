pipeline {

	agent {
		label {
			label "slave-1"
			customWorkspace "/mnt/project"
		}
	}	
	
	stages {
	
		stage ("stage-1") {
		
			steps { 
			
				sh "sudo yum install docker -y"
				sh "sudo systemctl start docker"
			//	sh "sudo echo "application of telemedia" >> /mnt
				sh "sudo run -itdp 80:80 --name httpd-1 httpd"
				sh "sudo cp /mnt/project/index.html httpd-1/usr/local/apache2/htdocs/"
				}
			}
		}




}
