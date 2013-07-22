
Git Presentation Notes
======================
by Margaret Scott (eudaimonious@gmail.com)

** Set up Git and GitHub **
https://github.com
https://help.github.com/articles/set-up-git#platform-mac

** What is a git repository? **
* The .git directory
* A set of commit objects
* A set of references to commit objects (“heads”)

** What is a commit object? **
* A set of files
* References to parent commit objects

** What is a head? **
* A reference to a commit object
* There is a default head in every repository. It's called master
* A repository can have any number of heads
* There will always be one and only one currently active head

** Let's create a Repository **
git init <newfoldername> or simply git init

** Create a file, stage it and commit it **
cd <newfoldername>
touch pyladies.py
git status
It's “Untracked”
git add “pyladies.py”
Git status
Git commit -m “Initial Commit”
Git status
Git log

** The three commands you'll use over and over **
Git add .
Git commit -m “Fix infinite loop”
Git push origin master

** Now let's get set up to share it online **
create a repo on github's website (or see pro-tip below)
git remote add origin git@github.com:<githubusername>/<reponame>.git

Pro-tip:
If you have curl installed, you can create a github repo from your command line. Check to see if curl is installed by typing curl --manual. The curl command for creating a github repo is 
curl -u '<githubusername>' https://api.github.com/user/repos -d '{"name":"<reponame>"}'

** Edit the file, stage, commit, push **
Xdg-open pyladies.py
Git add .
Git commit -m “Add some content”
Git push origin master

** Branching & Merging **
Git checkout -b mybranch
Git branch
Git checkout master
Git merge mybranch

** Working with someone else's repo **
* Make a copy:
Git clone git@github.com:<githubusername>/<reponame>.git
* Receive changes:
Git fetch
Git pull origin master
* Upload your changes:
Git push origin master 

** Learn More **
www.sbf5.com/~cduan/technical/git/‎