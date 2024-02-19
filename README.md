# Github Pages & Jekyll
- 2024.02.16 `14주차`

`Github Pages`  
Github에서 제공하는 아주 단순하게 특정 주소로 오는 요청에 대하여  
Repository의 파일들을 정적으로 전달하는 서비스다.

`Jekyll`  
Ruby를 이용해 만든 정적 웹사이트 생성기  
https://jekyllthemes.io/을 통해 블로그 양식을 가져올 수 있다.
1. 원하는 양식을 고른다. 
2. 해당 Repository에 가서 download zip을 한다.
3. 압축 해제 후, 기존 파일들을 삭제 후 해당 파일들을 넣는다.
4. 파일 편집 시작

## 실행 방법

1. 아래 2개의 명령어를 터미널에 입력한다.
```java
bundle install
bundle exec jekyll serve
```
2. `localhost:4000`을 `ctrl + click`한다.
3. 파일 확인 후, push를 해주면 자동으로 배포가 된다.

## 편집 방법

`_config.yml`
```markdown
title: # 탭 이름 설정
description: > # this means to ignore newlines until "baseurl:"
  # 링크 공유 시, 해당 링크 설명 워딩
permalink: ':title/'
baseurl: "" # the subpath of your site, e.g. /blog
url: "해당 URL을 적어준다." # the base hostname & protocol for your site, e.g. http://example.com
site-twitter: #if your site has a twitter account, enter it here

# Author Settings
author: # add your name
author-img: # add your photo
about-author:  # add description
social-twitter: # add your Twitter handle
social-facebook: # add your Facebook handle
social-github:  # Github 계정을 적어준다. Ex) fish-minkyu
social-linkedin: # add your Linkedin handle
social-email: # add your Email address
```

`/assets/img`
: 이미지 파일들은 해당 경로에 모두 모아놓는다.

`/assets/img/favicon`
: 탭에 나온 아이콘을 바꿀 수 있다.  
이 때, `favicon generator`로 검색을 해서 넣고자 하는 사진을 넣은 후, 다운 받은 파일들을 넣어준다. 

`/_posts`
```markdown
---
layout: # post를 넣으면 게시글 유형이 생성된다.
title: # 제목
date: # 생성 시간, 생성시간 날짜와 해당 마크다운 파일의 날짜가 같아야 한다. (시간은 +0900로 고정하는 것을 추천)
description: # 링크 공유 시, 해당 링크에 관한 설명글이 나온다. (optional)
img: # 게시글 표지 이미지 (optional)
fig-caption: # 게시글 태그(optional)
---

# 해당 게시글에 관한 내용 적기
```


