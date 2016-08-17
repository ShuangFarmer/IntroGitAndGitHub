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
 
- What are some situations when branches would be helpful in keeping your history organized? How would branches help?  

 If one wants to make some changes and doesn't want to apply it into the formal version (e.g., adding a new feature or fix a bug or doing something experimental), brances would be helpful.  
 
 A branch can develop independent of the master branch. When it is developed to a certain level, it is also able to be merged with the master branch. Branches helps developer make experimental changes boldly. It boosts innovation.  
 
 command:
 - run `git branch`, to view the branches of a respository, 
 - run `git branch branch_lable`, to create a new branch
 - run `git checkout branch_lable`, to check out a branch (go to and work on that branch) 
 - to create and check out a new branch simutanuouly, run `git checkout -b branch_name` 
 
- How do the diagrams help you visualize the branch structure?  

 It shows the tree-like structure of the respository. One are able to check at which point a branch is builr and how many commits that branch contains.
 
 command:  
 - run `git log --graph --oneline master branch_name`, to view the structure.  
 
- What is the result of merging two branches together? Why do we represent it in the diagram the way we do?  
 After merging, there is only one branch with all the commits from two original branches. Commits are ordered by its timestamps. That is also why we represents in the diagram in this way.  
 
 to merge branch_2 into branch_1: 
 - run `git checkout branch_1`  
 - run `git merge branch_1 branch_2` (`git merge` always merge all the specified branches into the currently checked out branch. Therefore one can also directly run `git merge branch_2`) . A new commit will be created for the merging.
 - run `git branch -d branch_2`, delete the already merged branch_2  
 
 bonus: to compare one commit with its parent  
 - run `git show`