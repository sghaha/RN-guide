# 생성된 프로젝트 살펴보기

## 엔트리 파일
> - index.js   
> 프로젝트의 시작점. 여기서 import를 통해 코드를 불러와 앱을 번들링.       
> App이라는 컴포넌트를 불러와서 AppRegistry.registerComponent라는 함수를 사용해서 컴포넌트를 등록   
> 최상단의 @format은 Prettier와 관련된것임. 코드 스타일 정리해줌   


## App 컴포넌트
> - App.tsx
> (원래는 App.js인데 나는 RN 프로젝트 생성할때 타입스크립트를 사용한다고 옵션을 넣어서 App.tsx가 된다. )    
> SafeAreaView, ScrollView, View, Text, StatusBar등이 import되어있는데 화면관련이다.   
> 맨 마지막 export default App; 부분에서 코드들을 export한다. 그래서 index.js에서 App을 가져다 쓸수 있는것임
