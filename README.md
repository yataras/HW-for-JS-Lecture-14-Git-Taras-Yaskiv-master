# HW-for-JS-Lecture-14-Git-Taras-Yaskiv
testing new project in github

# 0. 

Commits:

01: preparing data (first commit before branching. Adding main page.)

02: preparing data (second commit before branching. Adding files for styles and js code.)

03: preparing data (first commit in branch develop. Adding another index.html file)

04: preparing data (second commit in branch develop. Making some changes in index2.html file) 

Revert "05: preparing data (second commit in branch develop-feature1. Making some changes in index2.html file)"

05: preparing data (first commit in branch develop-feature1. Making some changes in style.css file)

06: preparing data (second commit in branch develop-feature1. Making some changes in index2.html file)

07: preparing data (first commit in branch develop-feature2. Making some addings changes in style.css file)

08: preparing data (second commit in branch develop-feature2. Conflict between develop-feature1 and develop-feature2 in style.css file)

09: preparing data (third commit in branch develop-feature1. Deleting index.html file)

Action with branches:

1) Merging changes from branch develop-feature1 to branch develop.

2) Merging changes from branch develop to branch master and marking resulting revision master with tag release1.

2) Removing branch develop-feature2 locally and from the server.


# 1.

Commands:

1)	$ git log --pretty=format:"%s [%an]" --since=3.hour.ago --branches=develop-feature1\ sort -r

2)	$ git log --pretty=format:"%s [%an] %cd" --branches=master\|develop --grep="05:"


# 2.

*git cherry-pick* помогает применить один-единственный коммит из одной ветки к дереву другой.

Для этого нужно выписать ветку, в которую будем вливать коммит:

git checkout master

Обновить ее:

git pull origin master

Выполнить команду, указать код коммита:

git cherry-pick <code of commit>

После этого обновить ветку на сервере:

git push origin master


# 3.

$ git commit -am "Typo"

$ git push

$ # Realize you had a typo, so push again but send HEAD^ upstream 

$ # ( HEAD^ means the HEAD at the previous commit )

$ git push -f origin HEAD^:master

$ git commit --amend -m "Fixed Typo"

$ git push # No pull or merge needed
