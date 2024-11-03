# useNavigate
## `useNavigate를 이용한 라우팅`
리액트에서 라우팅을 위해서는 ‘react-router-dom’ 모듈 설치 필요

브라우저의 상단 주소입력 부분의 주소를 변경시키기 위해서, useNavigate를 이용

- 사용방법
```jsx
import { useNavigate } from ‘react-router-dom’

(...)

const navigate = useNavigate()

(...)
navigate(-1) <-- 이전 페이지로 돌아감
```