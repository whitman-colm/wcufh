# _TAGME file guide

The `_TAGME` file is a very small file included within each folder. It contains  the couple things that go at the top of each folder's page. It is shittily parsed by `sed` within `updatesite` and `update` so there is no 'syntax' per se but the file needs to be set up as such:

```
FOLDERNAMESHORT
FOLDERNAMEFULL
FOLDERDESCRIPTION
```

So for instance, given the following `_TAGME`:

```
MAT 127 (XX)
Math 127 Section XX with Prof Smith
View previous labs and notes
```

Would format to this on the root `index.html`:

```
Site updates, yadda yadda
---
To Folder: MAT 127 (XX)
More info: View previous labs and notes
---
etc
```

and this on the class-specific page:

```
Math 127 Section XX with Prof Smith
Site updates at etc

go back
---
files and what else
```

Make sure the file is in `/classes/myfolder/_TAGME` or else the ghosts of all who died lost in a CLI will rise and add you to their ranks.

#EOF
