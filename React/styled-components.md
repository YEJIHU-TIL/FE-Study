# styled components

- 스타일은 유지하되 태그를 바꾸고 싶은 경우
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