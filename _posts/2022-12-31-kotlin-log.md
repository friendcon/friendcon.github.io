---
title: "[Kotlin/Spring Boot] Lombok 대신 로깅하기"
excerpt: "Kotlin+Spring Boot 환경에서 Lombok을 사용하지 않고 로그를 찍는 방법! 🕶"

categories:
  - Spring
tags:
  - [Spring, Kotlin]

permalink: /spring/kotlin-log/

toc: true
toc_sticky: true

date: 2022-12-31
last_modified_at: 2022-12-31
---

## 🦥 Kotlin + Spring Boot 조합에서 로그 출력하기

강의를 들으면서 Java/Spring 조합에서는 로깅을 위해 Lombok을 사용을 하던데.. 나는 Kotlin/Spring 으로 진행하고 있어서 로그를 찍기위한 라이브러리를 찾아봐야했다..

### 🌿 1. 로그 라이브러리 선택
```
    implementation("io.github.microutils:kotlin-logging-jvm:3.0.4")
```

### 🌿 2. 사용방법
```
    class PostController() {
        private val logger = LoggerFactory.getLogger(javaClass) ...

        fun get() {
            logger.info("get 요청입니다.")
        }
    }
```