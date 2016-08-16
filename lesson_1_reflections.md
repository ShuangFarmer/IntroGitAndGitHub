- How did viewing a diff between two versions of a file help you see the bug that
was introduced?

 It can pinpoint the location of the difference between two files fast and accurately.

- How could having easy access to the entire history of a file make you a more
efficient programmer in the long term?

 One can be more brave/bold to make changes in his codes and don't worry about screwing everything up.  
With version control, one can always go back to a more complete and conservative version. 

- What do you think are the pros and cons of manually choosing when to create a
commit, like you do in Git, vs having versions automatically saved, like Google
docs does?

 - pros:  
 It is flexible. Each logical change can be saved. Thus, one can track and manage the progress/history of his files better.   
 
 - cons:  
 The judgement on when to make a commit might be subjective and difficult.
 
- Why do you think some version control systems, like Git, allow saving multiple
files in one commit, while others, like Google Docs, treat each file separately?

  It depends on the kind of **change** one mihgt make. It is quite logical to allow saving multiple files in one commit, especially when one logical change is made by chaning multiple files (e.g., HTML + CSS). As for Google Docs, it usually deals with separate files. Thus, it is not necessary to save multple files in one commit.

- How can you use the commands git log and git diff to view the history of files?

  - run `git clone + reponsitory URL` to clone a respository
  - `cd` into one respository  
  - run `git log` to view the history of files  
  - find the **commit ID** for two files to be compared  
  - run `git diff commit_ID_1 (original) commit_ID_2 (new)` to see the difference  
  - plus: to get colorred diff output, run `git config --global color.ui auto` (`--global` means applying this setting to all the git repositories)

- How might using version control make you more confident to make changes that
could break something?  

  one can always run `git log` to view the history of files and run `git checkout commit_ID` to restore the old version. 

- setting up your Wokrspace  
  - download 3 files 「add link」 
    - git-completion.bash
    - git-prompt.sh 
    - bash_profile_course  
   
- move files into home directory  
  
		```  
		cd ~  
		mv Downloads/git-completion.bash git-completion.bash  
		mv Downloads/git-prompt.sh git-prompt.sh  
		```

- move git configuration files to home directory  
 
		```  
		mv Downloads/bash_profile_course .bash_profile  
		```  
- reopen terminal 

`bash_profile_course`    
 
- 指令补全 
 
		source ~/git-completion.bash  
		
- 定义将用到的颜色  

		green="\[\033[0;32m\]"
		blue="\[\033[0;34m\]"
		purple="\[\033[0;35m\]"
		reset="\[\033[0m\]"		
	
- 定制提示符（prompt）颜色  
		
		#load another file to allow git-related information to be shown in the prompt
		source ~/git-prompt.sh 
		
		# when files are changed, asteroids will show up 
		export GIT_PS1_SHOWDIRTYSTATE=1 
		
		# '\u' adds the name of the current user to the prompt
		# '\$(__git_ps1)' adds git-related stuff
		# '\W' adds the name of the current directory
		export PS1="$purple\u$green\$(__git_ps1)$blue \W $ $reset" 













  