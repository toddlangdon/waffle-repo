# waffle-repo
Repository for playing around with Waffle features and GitHub integration  

## Summary 

- Milestones...will represent Sprints  
- Labels....can be used to represent Themes, Epics, Backend, Frontend, Waiting, etc, etc.  
- Branches...will be used to represent and work on Stories (feature/42-name, fix/something, refactor/something-else)
- Pull Requests...will be used to facilitate code review of Stories before merge into develop branch  


## Process

Here is the basic GitHub process I believe we should follow:  http://hugogiraudel.com/2015/08/13/github-as-a-workflow/  

Then Waffle.io can just give a nice board view of what is being worked to facilitate our standups and also give client visibility  

### Steps 

1. Write Stories as Issues in GitHub (Backlog)  
	- Capture Acceptance Criteria in body  
2. Create Branch for each Story/Issue when work is ready to begin 
	- Example branch names: feature/42-teaser, fix/23-something, refactor/14-shitty-code)  
3. Issue empty commit on new Branches so that Pull Request can be created  
	- Command: git commit --allow-empty -m "Feature 42 Initial Commit"  
4. At GitHub.com create Pull Request from relevant (feature) branch to destination (develop)  
	- Name as name after feature and prefix with [WIP] (work in progress) or [RFR] (ready for review) for example "[WIP] Feature 42: teaser"  
	- Alternatively we could use labels to represent WIP and RFR  
	- In Description field use GitHub markup to create list of checkboxes/tasks (this is because GitHub is smart enough to show %complete  
5. Check off tasks on Pull Request as they are completed and committed to the feature branch  
6. Use GitHub inline comments to review code associated with pull request  
7. For standups/status reviews the Pull Request view can be used and various labels attached to corresponding Issues can highlight important things such as "Waiting"  




## References 
Some good articles on git-flow:    
	- http://gitolite.com/gcs.html    
	- http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/    
	- https://help.github.com/articles/github-flow-in-the-browser/  

