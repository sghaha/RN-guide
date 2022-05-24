# reactNavigation

## 1. 설치
- react-navigation/native
```
npm i @react-navigation/native
```
- react-navigation/native-stack
```
npm i @react-navigation/native-stack
```
- react-native-screens & react-native-safe-area-context
```
npm i react-native-screens react-native-safe-area-context
```
- pod-install : 맥 전용
```
npx pod-install
```


## 2. android MainActivity.java에 추가
android/app/src/main/java/{앱이름}/MainActivity.java에     
아래 import와 onCreate 함수 추가    


```
import android.os.Bundle;
...
@Override
protected void onCreate(Bundle savedInstanceState) {
  super.onCreate(null);
}
```
