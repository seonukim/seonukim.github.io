---
layout: post
title:  "[Scala] 작업 경로 확인/변경, 파일 확인"
date:   2022-08-16
categories: [Study]
tags: [scala]
---

#### 스칼라에서 현재 작업 중인 경로를 확인하고 변경하고 싶을 때, 아래 코드를 사용한다.
```scala
// 현재 디렉토리 확인
System.getProperty("user.dir")
```

#### 또한, 현재 작업 중인 경로를 변경하고 싶을 때, 아래와 같이 코드를 입력한다.
```scala
// 작업 경로 변경
System.setProperty("user.dir", "변경할 디렉토리")
```

#### 마지막으로, 현재 경로 내의 파일 리스트를 보고싶으면, 아래와 같이 코드를 입력한다.
```scala
// 현재 경로 내의 파일 리스트 확인하기

// java의 File 객체 호출
import java.io.File

val files = new File("디렉토리 경로")
for (file <- files.listFiles())
    println(file)
```

`Zeppelin`을 사용하여 `Spark`를 학습 중인데,
`Zeppelin Notebook` 상에서 바로 파일 및 경로를 확인할 수 있어서 편리하다.