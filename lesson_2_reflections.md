# lession 2 notes 

- What happens when you initialize a repository? Why do you need to do it?  

 `cd` into the file folder and run `git init` to initialize the repository. A `.git` file will be created to track the history versions of the files. The output is:  
	
	```  
	Initialized empty Git repository in /Users/Username/.../version-control/reflections/.git/  
	```  
	
  Note: files start with a `.` are hidden.  

- How is the staging area different from the working directory and the repository? What value do you think it offers?   

 It works somehow like cookies. One can temporarily put files on it before eventually making a commit. Maybe, one can continute to add files in the staging area or change their mind to delete them, which makes git system more flexible. 
	
- How can you use the staging area to make sure you have one commit per logical change?  

 - run `git diff` to compare files in `working directory` with files in the `staging area`. Note: Without adding new files, the information in the staging area is the same as the last commit in the respository.  
 - run `git diff --staged` to compare files in the `staging area` with the last commit in the `respository`.  
 - if not keeping the changes made in working directories as well as in the staging area, run `git reset --hard`  <- **Danger Alert**: this operation cannot be reverted