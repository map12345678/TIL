
---

### js 프로토타입?

클래스 기반의 언어에선 클래스 내부에 모든 속성과 메소드가 정의되어있다. 해당 클래스를 기반으로 한 객체가 인스턴스로 생성되면 이 객체는 클래스 내부에 정의되어있는 속성과 메소드에 접근하여 사용할 수 있는 형태이다.

`프로토타입`은 이런 클래스와 아주 유사하며 `javascript` 의 모든 객체 프로토타입은 값을 할당하는 시점에 결정된다. 

### 프로토타입 기반 언어

>
>   JavaScript는 흔히 프로토타입 기반 언어라고 불린다.
>

모든 객체들이 메소드와 속성들을 상속받기 위한 명세로 프로토타입 객체를 가진다는 의미이다.

클래스 처럼 객체의 인스턴스를 위한 명세와 같은 역할을 하는데 객체 본인만이 가진 속성과 메소드에도 접근할 수 있으면서 프로토타입의 것들에도 접근할 수 있다.

javascript에서 함수를 생성할 때 프로토타입 속성이 함수에 붙여진다.
예를 들어, `new`로 함수들을 호출 할 때마다 생성되는 인스턴스 함수 프로토타입의 모든 속성을 상속한다.

```javascript
const Hello = function(name) {
  this.name = name;
}
```

![](https://i.imgur.com/4Vmvwvv.png)

속성과 메소드들은 각 객체 인스턴스가 아니라 객체 생성자의 `prototype` 속성에 정의되어 있다.

`Hello` 에 정의한 `name` 멤버 외에 프로토타입 객체인 `o`