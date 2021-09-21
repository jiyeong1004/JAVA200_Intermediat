# Vue

**{{데이터}}** : 데이터를 있는 그대로 표시

**v-bind** : 요소의 속성을 데이터로 지정

**v-model** : 입력폼과 데이터의 연결

**v-on** : 이벤트 연결

**v-if** : 조건에 따라 표시

**v-for** : 반복해서 표시

**computed** : 데이터를 사용한 계산

**watch** : 데이터의 변화 감시

**transition** : 표시 / 바표시에 애니메이션 처리

**component** : 컴포넌트 조립

## < vue 인스턴스 작성 >

```JavaScript
new Vue({
	el : 어느 html 요소를 연결할 것인가
	data : 어떤 데이터인가
	methods : 어떤 처리를 하는가
	computed : 어느 데이터를 사용하여 계산하는가
	watch : 어느 데이터를 감시하는가
})
```
