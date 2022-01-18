# Get linux commands on windows

WSL. Windows Subsystem for Linux (WSL) lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications - 
	directly on Windows, unmodified, without the overhead of a traditional virtual machine or dual-boot setup. 
	This will give us access to more modern commandline interfaces on windows machines. 

	https://docs.microsoft.com/en-us/windows/wsl/install

# For BASH users. 
If the anaconda install overwrites your bash profile, add a source command to end of `~/.bashrc`
	
	if [ -f ~/.profile ]; then
    		source ~/.profile
	fi
