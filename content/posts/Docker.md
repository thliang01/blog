---
title: "Docker 101"
subtitle: ""
date: 2021-01-08T22:06:16+08:00
lastmod: 2021-01-08T22:06:16+08:00
draft: false
author: ""
description: "創建 建立 運行 移除 Docker 映像"

page:
    theme: "wide"

upd: ""
authorComment: ""

tags: ["Docker"]
categories: ["DevOps"]

hiddenFromHomePage: false
hiddenFromSearch: false

featuredImage: ""
featuredImagePreview: ""

toc:
  enable: true
math:
  enable: false
lightgallery: false
license: license = '<a rel="license external nofollow noopener noreffer" href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank">CC BY-NC 4.0</a>'
---

## 創建 建立 運行 移除 Docker
`$ cat app.py`

```python
from flask import Flask 

app = Flask(__name__)

@app.route('/') 

def hello_world():
    return 'Hello, World! (from a Docker container)' 
 
if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0')
```

## 建立 requirements.txt
`$ cat requirements.txt`
```
Flask
```

## 建立 Dockerfile
` $ cat Dockerfile`

``` Dockerfile
    FROM python:3.7.3-alpine
    
    ENV APP_HOME /app
    WORKDIR $APP_HOME
    
    COPY requirment.txt .
    
    RUN pip install -r requirements.txt
    
    RUN pip install --upgrade pip
    
    ENTRYPOINT [ "python" ]
    CMD [ "app.py" ]
```

## 建立 Dockerfile 映像檔
` $ docker build -t hello-world-docker .`

## 執行 docker images
` $ docker build -t hello.world-docker .`

## docker run
` $ docker run --rm -d -v `pwd`:/app -p 5000:5000 hello-world-docker`


## License
* This article is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
* Please contact me for commercial use.