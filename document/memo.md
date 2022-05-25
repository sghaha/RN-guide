# 메모

## display Name 말고 그냥 프로젝트 이름을 바꾸고 싶을때
> react-native-rename을 보고 어디를 바꿔야 하는지 하나씩 찾아내서 찾아야한다.    
> 그냥 프로젝트를 새로 만드는게 맘편할 수도 있다.   
> 
> https://github.com/junedomingo/react-native-rename    
> 여기인데 아마 그냥은 안돌아갈거다.
    
    
## 메트로 서버에서
> R 누르면 앱이 리로드 되고    
> D 누르면 각종 디바이스 관련 액션및 설정이 뜬다.(실제 기기에서는 흔들면 된다고한다)     


## 디버그
> 메트로 서버에서 D 누르고 Debug하면 크롬 개발자 모드같은게 뜬다     
> 근데 이게 network는 안좋아서 flipper를 쓴다고 한다(근데 이것도 초기 설정하는데 오래걸릴수도...)    

## flipper 플러그인 추천
> - flipper-plugin-async-storage : 로컬스토리지 개념
> - flipper-plugin-redux-debugger : 리덕스 액션하는걸 보여줌


## 앱 이름 변경(display Name)
> - /android/app/src/main/res/values/string.xml
> - app.json의 displyName
> - /ios/FoodDeliveryApp/Info.plist의 CFBundleDisplayName


## 정렬

> - justifyContent : 세로 정렬
> - alignItems : 가로 정렬     
> 값 : flex-start / center / flex-end     
> 예 : 세로 중앙, 가로 오른쪽 정렬 ) <View style={{justifyContent:'center', alignItems:'flex-end'}}></View>

## 버튼 종류
> 버튼 종류는 아래와 같다. 조금씩 다르니 상황에 맞게 쓰면 될듯   
> 안드로이드랑 아이폰이랑 맞추기 쉽게 하려면 그냥 Pressable쓰고 스타일로 하는게 나을거다   
> 주의) 클릭이벤트 거는것이 onClick이 아니라 onPress니까 혼동하지말자
> - Pressable
> - Button
> - TouchableNativeFeedback
> - TouchableWithoutFeedback
> - TouchableHighlight
> - TouchableOpacity   
