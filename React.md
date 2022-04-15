# React 

## useState : 상태 값 변경
- useState는 다음과 같이 두 가지 방법으로 사용할 수 있다.
  ```js
  setState(5);
  setState((counter) => counter + 1); // 함수형 업데이트
  ```
- 기존 값을 이용한 상태 값 변경 시 함수형 업데이트 사용을 권장
  - 이유 1. 안전성
  - 이유 2. 최적화(return 값이 이전 상태 값과 동일할 경우 리렌더링을 하지 않는다.) 

## React.Memo : props가 변하지 않으면 다시 렌더링되지 않도록 최적화하는 방법
```js
<Btn text={value} onCLick={onCLick} />
<Btn text="string" /> // Btn에 Memo 처리를 해주지 않으면 state가 바뀔 때 이 부분도 다시 렌더링된다.
```
