# Ref
일반 HTML에서 DOM요소에 이름을 달 때는 id 사용

리액트에서는 Ref를 이용하면 DOM 요소들을 직접 조작, 제어 가능

Ref는 Reference의 줄임말로 참조를 뜻함

Ref는 DOM을 직접 건드려야 할 때 사용

## `useRef`
함수 useRef를 이용해 Ref 객체 생성

const textRef = useRef()

`<input ref={textRef} value={text} onChange={handleOnChange} />`

## `input 태그에 ref 만들기`
```jsx
import { useRef, useState } from "react";

function Body() {
    const [text, setText] = useState("");
    const textRef = useRef();
    const handleOnChange = (e) => {
        setText(e.target.value);
    };
    const handleOnClick = () => {
        alert(text);
    };
    return (
        <div>
            <input ref={textRef} value={text} onChange={handleOnChange} />
            <button onClick={handleOnClick}>작성 완료</button>
        </div>
    );
}
export default Body;
```

## `useRef로 입력폼 초기화하기`
```jsx
import { useRef, useState } from "react";

function Body() {
    const [text, setText] = useState("");
    const textRef = useRef();
    const handleOnChange = (e) => {
        setText(e.target.value);
    };
    const handleOnClick = () => {
        alert(text);
        textRef.current.value = "";
    };
    return (
        <div>
            <input ref={textRef} value={text} onChange={handleOnChange} />
            <button onClick={handleOnClick}>작성 완료</button>
        </div>
    );
}
export default Body;
```

## `useRef로 포커스주기`
```jsx
import { useRef, useState } from "react";

function Body() {
    const [text, setText] = useState("");
    const textRef = useRef();
    const handleOnChange = (e) => {
        setText(e.target.value);
    };
    const handleOnClick = () => {
        if (text.length < 5) {
            textRef.current.focus();
        } else {
            alert(text);
            setText("");
        }
    };
    return (
        <div>
            <input ref={textRef} value={text} onChange={handleOnChange} />
            <button onClick={handleOnClick}>작성 완료</button>
        </div>
    );
}
export default Body;
```