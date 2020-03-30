---
title: += operator method 만들기
comments: true
categories:
   - graze
tags:
   - swift
   - operator
classes: wide
---
생각나는대로 기록하는 공간입니다. 정제되지 않은 글과 코드들이 많습니다.
{: .notice--info}

## += 로 좌표 증가시키기

swift 강의 과제 중에 += 연산자를 확장해서 좌표를 증감시키는 과제가 있어서 구현해보았다.

### 기본 문법

```swift
static func operator(parameter) -> ReturnType {
    statements
}
```

새 함수를 만드는게 아닌 기존의 연산자를 확장시키는 것이다.

### 코드 구현

검증을 위해 간단한 구조체를 만든다.

```swift
struct Point {
    var x: 0.0
    var y: 0.0
}

// 인스턴스 생성
var p1 = Point(x: 1.0, y: 2.0)
```

p1의 x, y 좌표에 각각 1씩 더해서 다시 p1에 할당하고 싶다. 하지만 아래와 같이 쓰게 되면 당연히 될리가 없다.

```swift
p1 += 1
```

그래서 operator method 로 += 를 확장한다.

```swift
extension Point {
    static func +=(left: inout Point, right: Int) -> Point {
        let IncreasePoint = left
        left.x += Double(right)
        left.y += Double(right)
        return IncreasePoint
    }
}

var p1 = Point(x: 1.0, y: 2.0)
p1 += 1
print(p1.x, p1.y)    // 2.0, 3.0
```

잘 동작한다. 새 연산자를 만드는게 아니므로 몇가지 주의해야 한다.

1. 기존 연산자의 우선순위, 결합법칙을 바꾸지 못한다.
2. 원래 기능과 동일, 유사하게 구현한다.
3. 기존 parameter 와 return 이 일치해야 한다.

## Ref
- [어서와! swift는 처음이지?](https://programmers.co.kr/learn/courses/)
