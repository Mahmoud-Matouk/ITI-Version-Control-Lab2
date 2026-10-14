## Create two branches (dev & test)
git branch -c dev
git branch -c test

## Create one file on each branch, and push this changes to the remote repo.
git switch dev
touch dev.txt
git add .
git commit -m "add dev.txt"

git switch test
touch test.txt
git add .
git commit -m "add test.txt"

## Merge this changes on Main branch and then push it to your remote main branch.
git switch dev
git merge test

git switch main
git merge dev
git push

## Tell me how to remove them locally and remotely.
git branch -d test
git branch -d dev

## Tell me how to checkout another branch without commit changes
git stash
git checkout test
git stash pop

## Create an annotated tag with tagname (v1.7) .
git tag v1.7

## Push it to the remote repository.
git push

## Tell me how to list tags.
git tag

## Tell me how to delete tag locally and remotely.
git push origin --delete v1.7

## Add an image in the README.md file.
![alt text](http://url/img.png)