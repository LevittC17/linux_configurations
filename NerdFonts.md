Installing Nerd Fonts
==
*<mark style="background: #FF5582A6;">Downloading nerd fonts from the webste</mark> [[nerdfonts.com]]*

I installed jetBrains mono fonts on my system, i really love how they look.

unzip the compressed folder using the commanad -->
	```sudo unzip JetBrainsMono-2.304.zip```

<mark style="background: #ABF7F7A6;">Find the ttf folder from the unzipped one and move it to your local fonts folder. In my case the folder is found in /usr/share/fonts.
I'm using BlackBuntu operating system.
move the file/folder with the following command:</mark>

		```sudo cp font_file.ttf /usr/share/fonts/truetype/```

Update the fc-cache by running the following command as root:
		``` sudo fc-cache -f -v```

Check whether the fonts have been installed by running the command ```fc-list``` on the terminal.
The command displays a list of all installed commands on your system.