pipeline {

	agent {
		label {
			label "slave-1"
			customWorkspace "/mnt/proj1"
		}
	}
	
	stages {
	
		stage ("stage-a") {
		
			steps { 
			
				//sh "sudo docker stop httpd-1"
				//sh "sudo docker rm httpd-1"
				sh "sudo docker volume creat index1"
				sh "sudo cp -r /mnt/proj1/index.html /var/lib/docker/volumes/index1/_data/"
				sh "sudo docker run -itdp 8080:80 -v index1:/usr/local/apache2/htdocs --name httpd-2 http"
				
				}
			}
		}




}
