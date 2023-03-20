Installing the apt repository
===
<mark style="background: #D2B3FFA6;">Update the</mark> `apt` <mark style="background: #D2B3FFA6;">package index and install packages to allow</mark> `apt` <mark style="background: #D2B3FFA6;">to use a repository over HTTPS:
</mark>
		`sudo apt-get update`
		`sudo apt-get install \
			ca-certificates
			curl
			gnupg
			lsb_release`

Add docker's official GPG key:
		`sudo mkdir -m 0755 -p /etc/apt/keyrings`
		`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg`

<mark style="background: #BBFABBA6;">Set up the repository with the following command:</mark>
		`echo \
		  `"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
		  `$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

Install the docker engine
---
<mark style="background: #CACFD9A6;">First, update the `apt` package index</mark>

		sudo apt-get update


Install Docker Engine, containerd, and Docker Compose
		`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`


<mark style="background: #FFB86CA6;">Verify the Docker Engine installation is successul by running the</mark> `hello-world` <mark style="background: #FFB86CA6;">image</mark>
		`sudo docker run hello-world`

Install an Ubuntu Image:
		`sudo docker run -it ubuntu bash`

The command pulls an ubuntu image from the docker hub and installs it in your system.
After installation, do a post install on the image as its done when installing a live linux image.
