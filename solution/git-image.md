# Exercise 2: add image to git

This exercise asks you to add a folder to your repo, and thereafter
image to that folder.  And finally commit everything to github!

1. make a new folder (e.g. _images_) to this repo.  Hint: `mkdir`

```
mkdir images
```

2. ensure that the folder is there.  Hint: `ls`

```
ls
```
(you should see folder "images" listed there among the other files)

3. download an image you like and save it into the image dir you made
   above.
   
(use your web browser or something)
   
4. on command line navigate to the image folder.  Hint: `cd`

```
cd images
```

5. ensure that the image is there.  Hint: `ls`

```
ls
```
(you should see the image file here.  no other files should be visible)

6. add the image to your git repo.  Hint: `git add image.jpg`

```
git add image.jpg
```
(or whatever is the name of your image.  Note: if it contains spaces,
then you need to put it into quotes like `git add "multi word file
name.jpg"`)

7. commit and push the changes.  Hint: `git commit -am ".. your
   message here.. ".
   
```
git commit -am "added image file"
git push
```
   
8. go and check on github that the image is there.

(the image folder should be there, and if you click there then you
should see the image too)

9. as before, edit this file and write here the commands you used.
   Hint: you have to do the edits and commit again, in a similar
   fashion as above.
   
do the edits and commit/push again:
```
git commit -am "added git commands"
git push
```

Did the edits show up on github?

(they should)
