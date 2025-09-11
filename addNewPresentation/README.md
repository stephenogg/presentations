# How to Add New Reveal Presentation to this repository

 The git repo is on my laptop @ /home/steve/presentations
The main branch of this repo on github is the origin of the repo on my laptop (`git add origin git@github.com/stephenogg/presentations.git`) and reveal is present as an upstream repo, with:
 - `git remote add upstream git@github.com:hakimel/reveal.js.git`
 - I can update reveal by `git pull upstream master`.
 	- Reveal repo main branch is still called "master"

Each presentation is a new branch. When finished, the branch gets merged with main and github pages deploys the main branch to the web. To open the new presentation, navigate to https://stephenogg.github.io/presentations/nameOfNewPresentation.html

This strategy allows me to open any other presentation by navigating to its \*.html file.

## SOP
Create a new branch named "newPresentation"
1.  `git checkout --orphan newPresentation`
2.  `git reset --hard`
   
Copy the html file containing the slides and any assets to the repo.

3. `cp newPresentation.html /home/steve/presentations`

At this point add other assets to the folders in the base folder.
Add all the new files to be tracked by git in this branch and commit these changes.

4. `git add .`
5. `git commit -m "message"`
   
Change back to the main branch

6. `git checkout main`

Merge the newPresentation branch with the main branch and push them to origin on github.com.

8. `git merge newPresentation`
9. `git push --all origin`

This *should* trigger a new build and deploy action on github to deploy the main branch to https://stephenogg.github.io/presentations

You just have to add the correct html file to the end of that URL to open the new presentation.






