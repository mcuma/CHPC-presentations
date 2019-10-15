# CHPC presentations main GIT page

To set up a repo with two remotes, one at github and another at CHPC gitlab, do the following:
```
$ git init
$ git add *
$ git commit -am "initial commit"
```
Now create empty repos both on github and CHPC gitlab, and once those are ready:
```
$ git remote add origin git@github.com:CHPC-UofU/CHPC-presentations.git
$ git remote set-url --add origin git@gitlab.chpc.utah.edu:training/chpc-presentations.git

```

## Use for other CHPC staff members


### Initial repo setup in your home
1. First clone the existing repo
```
$ git clone git@github.com:CHPC-UofU/CHPC-presentations.git
```
2. Add the other remote:
```
$ cd CHPC-presentations
$ git remote set-url --add origin git@gitlab.chpc.utah.edu:training/chpc-presentations.git
```
3. Add a new directory with files for the given presentation:
```
$ mkdir my-new-presentation
$ cp /path-to/my-presentation.pptx my-new-presentation
```
4. Commit the repository change and push it to the remotes
```
$ git commit -am 'added my-new-presentation'
$ git push origin master
```

### Updates of existing local repo
1. Make sure that the local and remote are synchronized:
```
$ git pull
```
merge if necessary.
2. Add/update some files
3. Commit the repository change and push to the remotes
```
$ git commit -am 'added my-new-presentation'
$ git push origin master
```


