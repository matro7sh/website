+++
title = "Interactive Shell"
date = "2021-02-03T21:49:20+02:00"
tags = ["shell", "cli", "python"]
categories = ["cli"]
banner = "img/banners/shellpreview.png"
summary = "A SMERSH command-line client"
author = "Jenaye"
+++

# How to use the python command line

>requirement : python >= 3.5

we recommend you to use alias like `alias smersh-cli='python3 /home/jenaye/dev/github/smersh-cli/main.py'`

```
smersh-cli http://localhost:8000
``` 

then enter your credentials ( by default if u used `make load-data`) you can try `jenaye/jenaye`

### How to display all data

> available entities : user, vuln, positivePoint, mission, negativePoint

```
SMERSH >> show mission 
╭────┬──────────────────────┬───────────────────────────┬───────────────────────────╮
│ ID │         Name         │        Start date         │         End date          │
├────┼──────────────────────┼───────────────────────────┼───────────────────────────┤
│ 1  │ FAKE-MISSION-EXTERNE │ 2020-11-08T23:16:51+00:00 │ 2020-11-13T23:16:51+00:00 │
│ 2  │ FAKE-MISSION-INTERNE │ 2020-11-08T23:16:51+00:00 │ 2020-11-13T23:16:51+00:00 │
╰────┴──────────────────────┴───────────────────────────┴───────────────────────────╯
``` 

### How to display details of target 

``` 
SMERSH >> show mission 1
╭────┬──────┬───────────────────────────┬───────────────────────────╮
│ ID │ Name │        Start date         │         End date          │
├────┼──────┼───────────────────────────┼───────────────────────────┤
│ 1  │ Yolo │ 2020-11-08T23:16:51+00:00 │ 2020-11-13T23:16:51+00:00 │
╰────┴──────┴───────────────────────────┴───────────────────────────╯
``` 

### How to add item 

>use `<entity>`  then : 

> `assign <field> '<value>'`

> finally `save` ( to make post request )

``` 
SMERSH - Mission[1] >> use user 
SMERSH - User[NEW] >> assign name 'toto'
SMERSH - User[NEW] >> assign username 'toto'
SMERSH - User[NEW] >> assign password 'toto'
SMERSH - User[NEW] >> assign roles add ROLE_ADMIN
SMERSH - User[NEW] >> assign roles add ROLE_USER
SMERSH - User[NEW] >> assign enabled true
SMERSH - User[NEW] >> save
The object was saved successfully
SMERSH - User[4] >> show
╭────┬──────┬─────────┬───────────────────╮
│ ID │ Name │ Enabled │ Assigned missions │
├────┼──────┼─────────┼───────────────────┤
│ 4  │ toto │   Yes   │       None        │
``` 

### Edit 

>use `<entity> <id>`  then  : 

> ` assign <field> '<value>'`

> finally `save` ( to make put request )

``` 
SMERSH >> use mission 1
SMERSH - Mission[1] >> assign name 'Yolo'
SMERSH - Mission[1] >> save
The object was saved successfully
SMERSH - Mission[1] >> show mission 1
╭────┬──────┬───────────────────────────┬───────────────────────────╮
│ ID │ Name │        Start date         │         End date          │
├────┼──────┼───────────────────────────┼───────────────────────────┤
│ 1  │ Yolo │ 2020-11-08T23:16:51+00:00 │ 2020-11-13T23:16:51+00:00 │
╰────┴──────┴───────────────────────────┴───────────────────────────╯
```

## Preview : 

![shell preview](/imgBlog/shellpreview.png)
