## children 속성은 리액트에서 컴포넌트의 자식 요소를 나타내는 속성입니다. 
컴포넌트 태그 사이에 넣은 내용을 props.children을 통해 조회할 수 있습니다. 이를 통해 컴포넌트가 자식 요소를 포함할 수 있습니다.

| children은 자식 요소를 포함할 수 있는 컴포넌트에서 사용 `<img>, <input>` 처럼 자식 요소를 포함할 없는 컴포넌트에서는 children을 사용 할 수 없음

부모 컴포넌트
```jsx
import React from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
  return (
    <div>
      <h1>부모 컴포넌트</h1>
      <ChildComponent>
        <p>이것은 자식 요소입니다.</p>
      </ChildComponent>
    </div>
  );
}

export default ParentComponent;
```

자식 컴포넌트
```jsx
import React from 'react';

function ChildComponent(props) {
  return (
    <div>
      <h2>자식 컴포넌트</h2>
      {props.children}
    </div>
  );
}

export default ChildComponent;
```
