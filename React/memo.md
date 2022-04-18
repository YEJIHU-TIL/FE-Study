# React.Memo

**props가 변하지 않으면 다시 렌더링되지 않도록 최적화하는 방법**

```js
<Btn text={value} onCLick={onCLick} />
<Btn text="string" /> // Btn에 Memo 처리를 해주지 않으면 state가 바뀔 때 이 부분도 다시 렌더링된다.
```
