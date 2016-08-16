# lession 2 notes 

- What happens when you initialize a repository? Why do you need to do it?  

 `cd` into the file folder and run `git init` to initialize the repository. A `.git` file will be created to track the history versions of the files. The output is:  
	
	```  
	Initialized empty Git repository in /Users/Username/.../version-control/reflections/.git/  
	```  
	
  Note: files start with a `.` are hidden.  

- How is the staging area different from the working directory and the repository? What value do you think it offers?   

 It works somehow like cookies. One can temporarily put files on it before eventually making a commit. Maybe, one can continute to add files in the staging area or change their mind to delete them, which makes git system more flexible. 
	