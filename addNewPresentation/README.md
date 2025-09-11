## Image Analysis with Fiji Workshop ##
A set of slides and training material written in HTML/CSS with the [Reveal.js](https://github.com/hakimel/reveal.js) framework to support a workshop on Image Analysis with Fiji for the [Centre for Developmental Neurobiology](https://devneuro.org)

A copy of the slides are currently hosted here: [https://stephenogg.github.io/presentations/imageAnalysisWithFiji.html](https://stephenogg.github.io/presentations/imageAnalysisWithFiji.html)

## Licencing and reuse ##
The [Reveal.js](https://github.com/hakimel/reveal.js) framework is used under the terms of the MIT licence.

The slide content and images (see exception below) are provided under a [CC-BY licence](https://creativecommons.org/licenses/by/4.0/). You may reuse the contents for any purpose in any way you please as long as you attribute the source material (see link for other licence terms).

## Acknowledgement ##
Original by [Dave Mason](https://mas.to/@dn_mason), from the University of Liverpool [Centre for Cell Imaging](http://cci.liv.ac.uk). Significantly changed and updated by [Stephen Ogg](mailto:stephen.ogg@kcl.ac.uk) from King's College London.



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






