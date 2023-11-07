# common-command-lines

### find things

find a file: 
```
find . -name "networkedge*" -print
```


### find and Delete directories built more than 3 days.
```
find . -depth -type d ! -name "conda" -mtime +3 -exec rm -rf {} \;
```

### check how many cores running on GCP.
```
squeue | grep R | wc
```
## remove recent folders:
```
find work -mindepth 2 -type d -cmin -1230 -exec rm -r {} \;
```
## cancle all the jobs:
```
squeue --me -h -o "%i" | xargs scancel

```
