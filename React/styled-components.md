# styled components

- 스타일은 유지하되 태그를 바꾸고 싶은 경우. `as` 사용

  ```js
  const Btn = styled.button`
    color: white;
    background-color: tomato;
    border: none;
    border-radius: 15px;
    padding: 10px 20px;
  `;
  ...
  <Btn>로그인</Btn>
  <Btn as="a" href="/">링크</Btn>
  ```
  <img width="156" alt="스크린샷 2022-04-18 오후 11 12 23" src="https://user-images.githubusercontent.com/39231606/163820524-29014171-a25b-4080-86a2-726dce243674.png">

- 속성값 설정 가능

  ```js
  const Input = styled.input`
    background-color: tomato;
  `;
  ...
  <Input required/>
  <Input required/>
  <Input required/>
  <Input required/>
  <Input required/>
  
  // 아래처럼 변경 가능
  const Input = styled.input.attrs({ required: true })`
    background-color: tomato;
  `;
  ...
  <Input/>
  <Input/>
  <Input/>
  <Input/>
  <Input/>
  ```

- 애니메이션

  ```js
  import styled, { keyframes } from 'styled-components';
  
  const rotation = keyframes`
    0% {
      transform: rotate(0deg);
      border-radius: 0;
    }
    50% {
      border-radius: 100px;
    }
    100% {
      transform: rotate(360deg);
      border-radius: 0;
    }
  `;
  
  const Box = styled.div`
    background-color: tomato;
    width: 200px;
    height: 200px;
    animation: ${rotation} 1s linear infinite; // 애니메이션 적용
  `;
  ```
