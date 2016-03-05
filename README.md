# Agile workflow
What agile workflow will be employed?

## Goals
Need to agree on a simple, but effective, agile workflow for this project

- Minimize the number of tools that must be used  
- Easy for team members to get in and start working on real things  
- Easy for both team members and product owners to see what is being worked on  

## Summary 

The source code for this application will be in a private GitHub repository so the team will focus on utilizing all the tools available when using GitHub, including Issues, Pull Requests, Milestones and Labels and the ability to comment and generally collaborate.  This document will explain the workflow the team will follow.  

	NOTE: There was some discussion about using Waffle.io or another tool that sits on top of GitHub and provides a story board view of things and we can do that; however, the focus will be on getting our workflow in GitHub right first.  

## Process

1. Write Stories to form Product Backlog  
	- Represented as Unassigned, Unmilestoned GitHub Issues  
	- Capture Acceptance Criteria in body    
	- Reviewed, refined, groomed on an ongoing basis with Product Owner  
	- Issues can be Labeled to indicate Theme and Priority 

2. Plan Sprint 
	- Apply Milestone to included Issues (stories) to build Sprint Backlog  
	- Label Issues to indicate Story Points  
	- Create Branch for each Issue (story) 		
		- Use git-flow naming convention: feature/42-teaser, fix/23-something, refactor/14-shitty-code  
		- Issue empty commit on new Branches (a hack - need at least one commit for Pull Request can be created)  
			- Command: git commit --allow-empty -m "Feature 42 Initial Commit"  
	- Create Pull Request for each included story 
		- Name to match story and most important includes "closes #42"  
			- referencing the Issue # will allow GitHub to automatically close Issues when PR is merged  
		- From Issue Branch to develop branch  
		- Use GitHub markdown checklists in PR body to Flesh out tasks  
		- Label with Milestone and as Work in Progress/WIP  

3. Start Sprinting  
	- Assign Issue to move from Sprint Backlog to In Progress  
		- Use Priority Labels as guide  
	- Tasks get Done
		- Means ready to share with team?  
		- Commit/push to story Branch 
		- Checkoff Tasks on Pull Request - GitHub will use this to show % complete  
	- Refine PR tasks iteratively as new work is realized, etc.  
	- Label Issues to indicate Waiting/Blocked
	- Stories (Issues) get Done
		- Means feature has unit tests and is working  
		- Label Pull Request as Ready for Review (and remove WIP Label)  
	- Review Code  
		- Pull Requests with the Ready for Review Label  
		- GitHub has tools for reviewing and commenting on commits   
		- Merge Pull Request 
			- Will close Issues as well and move to Done  
		
4. Sprint Status/Standups  
	- Review Milestone Pull Requests (% complete) to understand where Sprint stands  
	- Look for Labels like Waiting to identify things that must be addressed, etc.  


## References 
Some good articles on GitHub for agile:   

 	- [Zube.io blog post about using GitHub for agile workflow](https://zube.io/blog/agile-project-management-workflow-for-github-issues/)   
	- [http://gitolite.com/gcs.html](http://gitolite.com/gcs.html)
	- [http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/](http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/) 
	- [https://help.github.com/articles/github-flow-in-the-browser/](https://help.github.com/articles/github-flow-in-the-browser/)

	- [https://zube.io/blog/agile-project-management-workflow-for-github-issues/](https://zube.io/blog/agile-project-management-workflow-for-github-issues/)
