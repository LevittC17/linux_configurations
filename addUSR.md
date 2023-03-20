I want to add a user levitt on my docker container

Run the docker image:
	*<mark style="background: #FFF3A3A6;">sudo docker run -it ubuntu bash</mark>*

Update and install sudo command:
	*<mark style="background: #ADCCFFA6;">apt-get update && apt-get install -y sudo</mark>*

Create a new user and add it to the sudo group:
	*adduser levitt*
	*<mark style="background: #FFB8EBA6;">usermod -aG sudo levitt</mark>*

Swith to the newly created user
	*<mark style="background: #ABF7F7A6;">su - levitt</mark>*

Verify that you are now logged in to as the new user:
	*<mark style="background: #FF5582A6;">whoami</mark>*
