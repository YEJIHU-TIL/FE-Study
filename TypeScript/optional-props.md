# Optional Props

- 첫 번째 방법: ?? 연산자 활용
- 두 번째 방법: ES6 default params 활용

  ```ts
  interface CircleProps {
    bgColor: string;
    borderColor?: string;
    text?: string;
  }

  function Circle({ bgColor, borderColor, text = "default text" }) {
    return (
      <Container bgColor={bgColor} borderColor={borderColor ?? bgColor}>
        {text}
      </Container>
    );
  }

  export default Circle;
  ```
