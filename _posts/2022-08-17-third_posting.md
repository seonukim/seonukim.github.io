---
layout: post
title:  "[Docker] docker run 실행 시 에러 해결 사례"
date:   2022-08-17
categories: [Study, etc]
tags: [docker, container]
---

Docker를 활용하여 컨테이너 개발 환경을 구성하려는 중 마주한 에러이다.

```bash
docker load -i <image_name>
```

위 명령어로 이미지를 로드한 후,

```bash
docker run -d \
	-p 4000:4000 \
	-e <options>... \
	-name <container_name> ... \
	-volume=/your/dir:/dir \
	<image_name>:<imgae_tag> \
	/bin/bash ...
```


위 명령어를 실행했는데, 두번째 줄부터 에러가 났다.
에러 메시지는 `command not found` ..

잘못친 명령어가 없는데 뭐가 문제지.. 하고 한참을 씨름했는데
알고보니 개행 방식 때문이었다.


개행 방식은 OS에 따라 조금 차이가 있는데,
Windows에서는 `CRLF (\r\n)` 개행 문자를 사용하고,

Linux/Unix 계열에서는 `LF (\n)` 개행 문자를 사용한다.


윈도우 환경에서 컨테이너 실행 명령어를 shell script로 만들고
우분투 환경으로 옮겨서 그대로 사용했는데,

거기서 개행 문자의 차이 때문에 에러가 난 것 같다.


#### CRLF와 LF의 좀 더 자세한 정보는 구글링하면 많이 나온다.