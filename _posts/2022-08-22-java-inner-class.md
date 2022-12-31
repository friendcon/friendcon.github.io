---
title: "[Java] 내부 클래스 종류와 유형"
excerpt: "내부 클래스는 클래스 내부에 선언한 클래스로 외부 클래스와 밀접한 연관이 있는 경우가 많고 다른 외부 클래스에서 사용할 일이 거의 없을 때 사용"

categories:
  - Java
tags:
  - [Java]

permalink: /java/java-inner-class/

toc: true
toc_sticky: true

date: 2022-08-22
last_modified_at: 2022-08-22
---

## 🦥 내부 클래스

* 클래스 내부에 선언한 클래스로 외부 클래스와 밀접한 연관이 있는 경우가 많고 다른 외부 클래스에서 사용할 일이 거의 없을 때 사용한다
* 중첩 클래스라고도 하고 인스턴스 내부 클래스, 정적 내부 클래스, 지역 내부 클래스, 익명 내부 클래스가 존재한다.

### 1. 인스턴스 내부 클래스
* 내부적으로 사용할 클래스를 `private` 로 선언하는 것을 권장
* 외부 클래스가 생성된 후 생성
* private 으로 선언되지 않은 내부 클래스는 다른 외부 클래스에서도 생성할 수 있음

### 2. 정적 내부 클래스
* 외부 클래스 생성과 무관하게 사용할 수 있음
* 정적 변수, 정적 메서드를 사용해야함

### 3. 지역 내부 클래스
* 지역 변수와 같이 `메서드 내부에서 정의`하여 사용하는 클래스
* 메서드의 호출이 끝나면 메서드에 사용된 지역변수의 유효성은 사라짐
* 메서드 호출 이후에도 사용해야 하는 경우가 있을 수 있으므로 지역 내부 클래스에서 사용하는 메서드의 지역 변수나 매개 변수는 final 로 선언됨

### 4. 익명 내부 클래스
* 이름이 없는 클래스
* 클래스 이름을 생략하고 하나의 인터페이스나 하나의 추상 클래스를 구현해서 반환
* 인터페이스나 추상 클래스 자료형의 변수에 직접 대입하여 클래스를 생성하거나 지역 내부 클래스의 메서드 내부에서 생성하여 반환 할 수 있음