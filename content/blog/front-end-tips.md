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


First run `docker-compose up api` to be able to consume the API. Indeed you have to run `make install` first to setup the containers

 
# How to run Angular

As running javascript in a container is really slow we chose to not provide a container, then you have to go to the `client` folder and run the following command: 

``` 
npm i && npm start
```

the app will be available at : `http://localhost:4200` with hot reload.

Now you can work on your branch and submit pull request.