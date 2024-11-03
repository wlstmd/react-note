# state
state는 컴포넌트 내부에서 바뀔 수 있는 값을 의미

props는 컴포넌트가 사용되는 과정에서 부모 컴포넌트가 설정하는 값이며, 컴포넌트 자신은 해당 props를 읽기 전용으로만 사용 가능

props를 바꾸려면 부모 컴포넌트에서 바꿔줘야 하지만, 사용자의 행위나 시간 변동에 따라 값이 변할 수 있는 것을 state

state는 상태라는 뜻으로, 상태의 변화에 따라 값이 변하는 것처럼 리액트 컴포넌트 또한 state 값에 따라 다른 결과를 렌더링할 수 있음

## `state의 기본 사용법`
함수 useState로 state 생성 가능

`const [light, setLight] = useState('off');`

## `props & state`
props : 부모 컴포넌트가 설정
state : 컴포넌트 자체적으로 지닌 값으로 컴포넌트 내부에서 값 업데이트 가능