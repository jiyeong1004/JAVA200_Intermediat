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

## 싱글 파일 컴포넌트(Single File Components) 체계

- .vue 파일로 프로젝트 구조를 구성하는 방식

- 확장자 .vue 파일 1개는 뷰 애플리케이션을 구성하는 1개의 컴포넌트와 동일하다.

## .vue 파일의 기본 구조

```jsx
<template>
	<!-- HTML 태그 내용 -->
</template>

<script>
export default {
	// 자바스크립트 내용
}
</script>

<style>
	/* CSS 스타일 내용 */
</style>
```

### 화면에 표시할 요소들을 정의하는 영역

ex) HTML + 뷰 데이터 바인딩

```html
<template>
	<!-- HTML 태그 내용 -->
</template>
```

### 뷰 컴포넌트의 내용을 정의하는 영역

ex) template, data, methods 등

```jsx
<script>
export default {
	// 자바스크립트 내용
}
</script>
```

### 템플릿에 추가한 HTML 태그의 CSS 스타일을 정의하는 영역

```css
<style>
	/* CSS 스타일 내용 */
</style>
```

- v-bind + props : 상위 컴포넌트에서 하위 컴포넌트로의 데이터 전달

- v-on + $emit : 하위 컴포넌트에서 상위 컴포넌트로 데이터 전달
