---
layout: post
title:  "서버 개발 환경 구축 메모"
date:   2020-07-07 13:09:50 +0900
categories: jekyll update
---

# 나의 서버 개발 환경 구축 

## Ubuntu 

boost  

``` bash
sh bootstrap.sh 

./b2 --reconfigure stage toolset=gcc cxxflags="-std=c++1z -fPIC -O3 -Werror -Wno-unused-local-typedef -Wno-deprecated-declarations -Wno-unused-function" link=static,shared variant=release threading=multi linkflags="-fPIC"

sudo ./b2 install
```

flatbuffers
``` bash
cmake -G "Unix Makefiles" && make && sudo make install
```

MySQL Library  
[Download](https://dev.mysql.com/downloads/connector/cpp/)

NodeJs
``` bash
curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
sudo sh nodesource_setup.sh
sudo apt install nodejs
node -v
```


## MacOS

> boost  
```
brew install boost
```

> flatbuffers   
```
brew install flatbuffers
```


> MySQL Library    
[Download](https://dev.mysql.com/downloads/connector/cpp/)


> NodeJS
```bash
brew install nodejs
```

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
