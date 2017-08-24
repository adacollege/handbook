# Student Notebook Assignment Workflow

1. Go to the github repo link
2. Press 'fork' to create a copy on your own github account:

![fork](http://i.imgur.com/Mz2kkE3.png)

3. Copy the clone URL of your own copy - it should include your github username

![clone url](http://i.imgur.com/6NO0SKN.png)

4. Log in to Jupyter and open a new terminal (New -> Terminal). Run:
```sh
git clone <the url you copied>
cd <name of repo>
```
(to copy into a Jupyter notebook use SHIFT+CTRL+V)
5. Complete the assignment. Make sure you save your changes!
6. Commit and push your files:
```sh
git add --all
git commit -m 'your commit message'
git push
```
7. On your fork of the repo on github, press the 'new pull request', then the 'create pull request' button

![new pr](http://i.imgur.com/YDhd71F.png)
![create pr](http://i.imgur.com/NxRqjA2.png)

8. Submit your pull request to complete the assignment! Make sure to set the title of the PR to your name - lastname firstname:

![pr dialogue](http://i.imgur.com/zp5AaDa.png)

9. Your code will be tested automatically, and once it's done will show either a green tick or red cross

![travis test](http://i.imgur.com/hNrYYS8.png)
