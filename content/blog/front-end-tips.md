+++
title = "How to contribute as Angular developper"
date = "2021-02-07T21:49:20+02:00"
tags = ["angular", "npm"]
categories = ["front"]
banner = "imgBlog/preview/missionView.png"
summary = "tips for front-end developper"
author = "Jenaye"
+++

# How tp run API to work correctly

>requirements : node & docker + docker-compose

In case you want to contribute on the client part of the application it is useless to launch the codimd or the bitwarden, you just have to launch the API.


you can do it this way `docker-compose up api`

 
# How to run Angular

For the Angular part, you have to go to the `Client` folder and launch the following commands: 

``` 
npm i && npm start
```

the app will be available at : `http://localhost:4200` with hot reload.

Now you can work on your branch and submit pull request.