{
  "language": "go",
  "sudo": "required",
  "services": [
    "docker"
  ],
  "before_install": [
    "docker build registry.heroku.com/\"$HEROKU_APPNAME\"/web",
    "docker login -u \"$HEROKU_EMAIL\" -p \"$HEROKU_APIKEY\" registry.heroku.com",
    "docker push registry.heroku.com/\"$HEROKU_APPNAME\"/web"
  ],
  "group": "stable",
  "dist": "trusty",
  "os": "linux"
}







# v2hero  [![Build Status](https://travis-ci.org/sciman/v2hero.svg?branch=core-3.1)](https://travis-ci.org/csiman/v2hero)

本项目是一个利用Travis-CI部署Docker到Heroku 的学习示例。
