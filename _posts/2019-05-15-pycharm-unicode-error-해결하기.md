---
title: pycharm unicode error 해결하기
comments: true
categories:
   - python
tags:
   - python
   - ide
   - pycharm
   - utf8
classes: wide
---

mac OS 환경에서 pycharm - preferences의 encoding 설정을 utf-8로 했는데도 아래 코드를 실행시
<mark>UnicodeEncodeError: 'ascii' codec can't encode characters</mark> 와 같은 형태의 에러를 볼 수 있다.

```python
with open("vocabulary.txt", "r") as f:
    for line in f:
        prin(line)
```
encoding="utf-8" 을 인자로 넣어주면 해결되지만 문제가 생길때마다 하는 건 비효율적일 것이다.
pycharm이 LC_CTYPE 인식하지 못하는 것 같으니 pycharm terminal 옵션에서 LC_CTYPE을 직접 넣어준다.

1. File - Preferences에서Tools를 검색하고 Terminal로 이동
2. 아래 이미지와 같이 `LC_CTYPE`에 `ko_KR.UTF-8` 을 입력 후 OK 클릭

간단한 과정을 거쳐 pycharm을 종료 후 재실행 시키면 말끔히 해결된다.

![pycharm](https://d2ddoduugvun08.cloudfront.net/items/1K0J452L2K22413L1e2v/2019-03-29_14-43-53.png)

## References
---
[링크](https://hashcode.co.kr/questions/5306/pycharm-에서-한글-사용할-때-encoding-문제가-발생합니다)