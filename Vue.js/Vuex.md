## < Vuex의 4가지 속성 >

- **state** : 공유한 상탯값 데이터 정의

- **mutations** : setters의 의미로 이해하면 좋으며 외부에서 동기 방식으로 저장할 때 사용

- **getters** : state의 데이터값을 외부에서 읽어 올 때 사용

- **actions** : 외부의 API 실행 같은 비동기 실행을 관리할 때 사용


## < 상태 관리 패턴>

### 상태 관리 구성 요소

- **state** : 컴포넌트 간에 공유할 **data**

- **view** : 데이터가 표현될 **template**

- **actions** : 사용자의 입력에 따라 반응할 **methods**

```jsx
new Vue({
  // state
  data() {
    return {
      counter: 0
    };
  },
  // view
  template: `
    <div>{{ counter }}</div>
  `,
  // actions
  methods: {
    increment() {
      this.counter++;
    }
  }
});
```

- 단방향 흐름 처리

**View → Actions → State** → View → Actions → State → ...