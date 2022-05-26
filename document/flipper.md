
# Flipper 세팅

## Flipper 설치
https://fbflipper.com/

## Setup Doctor
> 오른쪽 Setup Doctor 버튼을 눌러서 ok가 아닌부분은 해결해줘야한다.
> 
> ### 1. android sdk
> 왼쪽 아래 세팅 클릭 - Android SDK location에 아래와 같이 입력   
> (마지막에 / 를 꼭 넣어야 하는듯)
> ```
> /Users/{아이디}/Library/Android/sdk/
> ```
> Apply and Restart 클릭
> 
> ### 2. IDB installed
> 아래와 같은 메시지가 뜬다   
> > IDB is required to use Flipper with iOS devices. It can be installed from https://github.com/facebook/idb and configured in Flipper settings. You can also disable physical iOS device support in settings. Current setting: /usr/local/bin/idb isn't a valid IDB installation.
> ```
> brew tap facebook/fb
> ```
> ```
> brew install idb-companion
> ```
> ```
> npm i react-native-flipper redux-flipper rn-async-storage-flipper @react-native-async-storage/async-storage
> npx pod-install # 아이폰 전용
> ```
> 이거 근데 리액트 버전이 68이라서 설치가 잘 안되는 느낌..
