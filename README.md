{
  "language": "go",
  "sudo": "required",
  "services": [
    "docker"
  ],
  "before_install": [
    "docker build -t registry.heroku.com/\"$HEROKU_APPNAME\"/web .",
    "docker login -u \"$HEROKU_EMAIL\" -p \"$HEROKU_APIKEY\" registry.heroku.com",
    "docker push registry.heroku.com/\"$HEROKU_APPNAME\"/web"
  ],
  "group": "stable",
  "dist": "trusty",
  "os": "linux"
}







# v2hero  [![Build Status](https://travis-ci.org/sciman/v2hero.svg?branch=core-3.1)](https://travis-ci.org/csiman/v2hero)

本项目是一个利用Travis-CI部署Docker到Heroku 的学习示例。

如果为您的学习提供了帮助，欢迎给一个Star ^_^

* 部署方法
   https://github.com/onplus/v2hero/wiki/Deploy-V2ray-To-Heroku
  
* 提问&建议
   https://github.com/onplus/v2hero/issues
   发起issue前请尽量先使用文档和搜索

* 相关项目
   https://wsss.herokuapp.com/

* 实现参考 
   - https://github.com/v2ray/v2ray-core
   - https://github.com/wangyi2005/v2ray
   - Heroku https://devcenter.heroku.com/articles/container-registry-and-runtime
   - Travis-CI https://docs.travis-ci.com/user/docker
