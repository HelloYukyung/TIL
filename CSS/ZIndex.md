# Z-index

보통, html파일을 x-y의 평면이라고 생각한다.
이때, Z-index는 x,y 평면에 z값을 주어 추가적인 레이어를 생성할 수 있게 해준다.

z-index 값을 따로 설정하지 않으면 기본 값은 0이며, z-index 값이 클수록 위쪽에 보이게 된다.

z-index는 position 속성과 함께 쓰인다.

## position

position 속성은 문서 상에 요소를 배치하는 방법을 지정한다.

### value

- static(초기값) : 요소를 일반적인 문서 흐름에 따라 배치 <br/>(z-index속성이 아무런 영향을 주지 못함)

- relative : 요소를 일반적인 문서 흐름에 따라 배치하고, 자기 자신을 기준으로 값에 따라 오프셋을 적용한다.

- fixed : 요소를 일반적인 문서 흐름에서 제거하고, 페이지 레이아웃에 공간도 배정하지 않는다.

```jsx
<AppBar position="fixed" sx={{ zIndex: (theme) => theme.zIndex.drawer + 1 }}>
  '''
</AppBar>
```

앱바 아래는 잘림 => AppBar가 모든 모달 보다 우선시 됨
