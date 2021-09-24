## 🎀 이벤트 버스 형식

- 이벤트 버스를 구현하려면 애플리케이션 로직을 담는 인스턴스와는 별개로 새로운 인스턴스를 1개 더 생성하고, 새 인스턴스를 이용하여 이벤트를 보내고 받는다.

- `.$emit()` : 보내는 컴포넌트

- `.$on()` : 받는 컴포넌트

### 👀 구현 형식

```jsx
// 이벤트 버스를 위한 추가 인스턴스 1개 생성
var eventBus = enw Vue();
```

```jsx
// 이벤트를 보내는 컴포넌트
methods: {
	메서드명: function() {
		eventBus.$emit('이벤트명', 데이터);
	}
}
```

```jsx
// 이벤트를 받는 컴포넌트
methods: {
	created: function() {
		eventBus.$on('이벤트명', function(데이터);
	}
}
```

### 👍 이벤트 버스 구현하기

[doit-vuejs/index.html at master · jiyeong1004/doit-vuejs](https://github.com/jiyeong1004/doit-vuejs/blob/master/exam/03/03-10/index.html)