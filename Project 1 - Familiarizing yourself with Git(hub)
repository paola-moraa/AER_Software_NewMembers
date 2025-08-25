Steps:
1. Make sure you have joined the “controls-software” slack channel
2. Create a GitHub Account
	1. I would recommend using a non-school, professional-looking email address to create this account
		1. You can add more email addresses after this if you’d like, but make sure the primary email address is a professional, non-school address
	2. If I get any requests from funny-sounding email addresses, I will kindly ask you to create a new account :)
3. Once you've created an account, send me a DM on slack with you full name, github username, and github email address
	1. Then you should come up to me so I can add them to the github project
4. Setting up environment
	1. All members of the software team will be interacting with github through WSL or a unix-based command line (mac/linux)
	2. The following steps will be divided into Mac and Windows portions, respectively
		1. Windows
			1. For those running windows, follow [this](https://learn.microsoft.com/en-us/windows/wsl/install) tutorial to install wsl
				1. Please just use the default installation steps, Ubuntu is very user-friendly and it will be easier if we are all working in the same environment
				2. Once WSL is installed, you will be asked to reboot your computer for it to finish installing. When you are rebooting, press F10, Enter, or whichever button puts you into the BIOS mode ([this](https://support.microsoft.com/en-us/windows/enable-virtualization-on-windows-c5578302-6e43-4b4b-a449-8ced115f58e1) link might help) and make sure you enable Virtualization. 
				3. Then, once you're back in windows, make sure to turn on the "Virtual Machine Platform" feature, as specified in the previous [link](https://support.microsoft.com/en-us/windows/enable-virtualization-on-windows-c5578302-6e43-4b4b-a449-8ced115f58e1)
			2. Once you have wsl installed, create a “Project” folder in your windows filesystem (preferably in your C:\\ or C:\\Documents\\ folder)
			3. Then, back in WSL create a [symbolic link](https://www.howtogeek.com/287014/how-to-create-and-use-symbolic-links-aka-symlinks-on-linux/) to that folder in your home directory
				1. hint 1: your C drive (displayed like "C:\\Stuff\\..." in windows) is displayed using linux notation in wsl ("/mnt/c/stuff/...")
				2. hint 2: You want to symbolically link a folder in a windows filestructure (using linux notation, see hint 1), to a new folder in a linux filesystem in wsl
				3. hint 3: your home directory in linux is shortened to "~" on the command line, but using `pwd` you can see that it is actually "/home/userName/"
				4. hint 4: the final filepath in wsl will be "/home/userName/Project/"
				5. Note: [Here](https://peter-whyte.com/create-a-link-between-local-windows-files-and-wsl/) is another resource that might help
			4. If all else fails...
				1. There is also a way to create a windows shortcut between your windows filesystem and wsl through the windows file explorer, but I haven't tried it. If you get it working, please show me how you did it and I'll add it here to the instructions :)
		2. Mac
			1. Create a "Project" folder in a directory that you have easy access to and won't forget about
	3. Create & Link SSH Keys
		1. If you have never created or used SSH Keys before, follow [this tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux) to create them
		2. Once you've created your SSH keys, link them to your GitHub account as shown in [this tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=webui)
		3. Notes
			1. Your SSH keys should automatically be stored in your `~/.ssh/` folder
			2. Github is asking you to add the contents of your public key file, make sure the output looks like the example on that page
			3. Mac users, apparently there's an additional step you might have to complete where you have to edit your `~/.ssh/config` file to tell your ssh-agent to automatically load your ssh keys, be sure to do so
	4. Test
		1. clone the github repo to your new project folder to make sure you ssh keys work (you will most likely be asked to set your git username and email address here, just make sure you use the same username and email address that you used for your github account)
			1. Note: Make sure you clone the repo using SSH, not HTTPS! SSH is the only way for you to authenticate using the keys you created a few steps before, and to be able to contribute to the repository
		2. Note: You will not be able to contribute to the repository (in your own branch I hope ;) ) until you accept my invitation to be added as a collaborator on github, you should see an email about it in the inbox of whichever email address you have associated with your github account
5. Github Project
	1. Each new member will create a new Pull Request with its own NEW branch, and it will refer to the existing "# New Member Project #1" issue
		1. On repository website, navigate to "Pull Requests", and then select "New Pull Request"
		2. When creating your pull request, make sure that it targets the specified issue, and that you create your own branch for the PR
			1. Please name your branch "firstName_lastName_PR"
			2. Note: [This](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue) link shows how to attach a pull request to a given issue, I've gotten feedback from members saying that the keyword "fix" was what they used to link their PR to the existing issue, so start there!
	2. Once you have created your pull request, create a new Markdown document (preferably using [Obsidian](https://obsidian.md/download) ;) ) 
		1. Use the format `firstName_lastName_Project1.md`
		2. In this document, I want you to list your first and last name, your major, and your previous programming experience
		3. I also want you to look through the New Member Projects document and list out which projects you would be most interested in contributing to, including any potential new projects that weren't listed!
		4. Formatting isn't super important, just make it pretty, and remember that you will be presenting from this document at next Monday's meeting! (the 23rd)
	3. When we meet next on the 23rd, I am going to be asking everyone to present from their uploaded file, roughly 5 minutes per person
6. Working with GitHub
	1. Don’t use “git add -A" or "git add \*", I am guilty of this, but it can add untracked files that are auto-generated by your development environment, which can then be difficult to remove once they’ve been committed
	2. I will be denying pull requests that include unnecessary files, I do not do this to hurt your feelings, I am only doing this to make sure we are only tracking source code (yes I am hypocritical, extra credit if you can find where in the git history for this repository I accidentally made that same mistake)
7. Resources
	1. Tutorials
		1. [W3schools.com](https://www.w3schools.com/git/default.asp)
		2. [Learn Git Branching](https://learngitbranching.js.org/)
	2. YouTube videos
		1. [How Git Works](https://www.youtube.com/watch?v=e9lnsKot_SQ)
		2. [Git Merge vs Rebase](https://www.youtube.com/watch?v=0chZFIZLR_0)
