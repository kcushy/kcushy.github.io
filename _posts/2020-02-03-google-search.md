---
title: 구글 검색 연산자 활용하기
comments: true
categories:
   - graze
tags:
   - google
   - tip
classes: wide
---

## 입력한 문장 그대로 검색하기

- 보통 A B C 라고 검색하면 A or B or C 가 포함된 페이지가 출력된다. 하지만 A and B and C + 단어 순서까지 그대로 반영된 채 검색이 필요할 때도 있다. 이럴 땐 큰 따옴표로 묶어서 검색한다.

- 적용 전

  ![tip-1]({{ site.url }}{{ site.baseurl }}/assets/images/google-tip-1.jpg)

- 적용 후

  ![tip-2]({{ site.url }}{{ site.baseurl }}/assets/images/google-tip-2.jpg)

## 고정된 단어 + 아무 단어 검색하기 

- "A B C" 라고 입력하면 A B C 가 그대로 검색되지만, "A * C" 와 같이 Asterisk(*)을 포함하면 A C 사이에는 아무 단어나 포함시켜 검색된다.

  ![tip-3]({{ site.url }}{{ site.baseurl }}/assets/images/google-tip-3.jpg)

## 특정 단어 제외시키기

- "A B C" 로 검색을 했는데, 불필요한 단어가 포함되서 검색이 되어 정밀도가 떨어질 수 있다. `-단어` 를 이용하여 검색한다. 

  ```
  e.g. "A B C" -D
  ```

## 특정 웹사이트 주소에서 검색

- `site:주소`를 이용한다.

  ```
  e.g. A B C site:google.com
  ```

## 확장자 지정하여 검색하기

- `filetype: 확장자`를 사용한다

  ```
  e.g. data structure filetype:pdf
  ```

## Ref

- [[도서] IT 개발자의 영어 필살기](http://www.kyobobook.co.kr/product/detailViewKor.laf?ejkGb=KOR&mallGb=KOR&barcode=9791189909093&orderClick=LAG&Kc=)

