# 1. 개발 환경 구축 (Mac)

## 1.0 homebrew 설치

### 1.0.1 homebrew 설치확인
터미널에서
```
which brew
```
결과값 나오면 아래 설치 안해도됨

### 1.0.2

https://brew.sh/
여기에 나온대로 아래 명령어 수행

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```


## 1.1. java 11 설치
왠지는 모르겠지만 11버전을 하라고 한다. 

### 1.1.1 다운로드 & 설치

> 나는 Amazon Corretto를 다운로드 한다.    
> 아래 url에서 11버전 다운받고 설치    
> (그냥 구글링해서 받아도된다.)    
>
> ```
> https://aws.amazon.com/ko/corretto/?filtered-posts.sort-by=item.additionalFields.createdDate&filtered-posts.sort-order=desc
> ```

### 1.1.2 자바 버전 확인
> 터미널에서
> ```
> java -version
> ```
> 안타깝게도 나는 지금깐 자바가 아니라 다른걸 보고있더라


### 1.1.3 자바 버전 변경
> 터미널에서 (vi 안쓰고 그냥 변경해도된다.)
> ``` 
> vi ~/.bash_profile
> ```
>     
> 맨밑에
> ```
> export JAVA_HOME=/Library/Java/JavaVirtualMachines/amazon-corretto-11.jdk/Contents/Home
> export PATH=${PATH}:$JAVA_HOME/bin
> ```
> 를 추가하자.    
> 중간에 경로는 내 java 경로인데 대충 비슷한 곳에 있을거다.


### 1.1.4 적용

> ```
> source ~/.bash_profile
> ```

### 1.1.5 확인

> ```
> java -version
> ```
>    
> - 결과
> ```
> openjdk version "11.0.15" 2022-04-19 LTS
> OpenJDK Runtime Environment Corretto-11.0.15.9.1 (build 11.0.15+9-LTS)
> OpenJDK 64-Bit Server VM Corretto-11.0.15.9.1 (build 11.0.15+9-LTS, mixed mode)
> ```


## 1.2 Node & Watchman 설치

https://reactnative.dev/docs/environment-setup
이걸 따라서 해도된다.   

```
brew install node
```

```
brew install watchman
```



## 1.3 Xcode

### 1.3.1 Xcode 설치
> Xcode설치가 안되어있으면 진행하다가 트러블이 나드라    
> App Store에서 설치하자

### 1.3.2 설정
> https://stackoverflow.com/questions/58998884/c-compiler-cannot-create-executables-installing-cocoapods
>
> 여기서 보이는 것처럼   
> 설정 - Loctions에서    
> Command Line Tools에 Xcode를 지정해준다


## 1.4 CocoaPods

### 1.4.1 설치

```
sudo gem install cocoapods
```


### 1.4.2 for M1 chip
Mac M1 아키텍처는 Cocoapods와 직접 호환되지 않습니다. 포드를 설치할 때 문제가 발생하면 다음을 실행하여 해결할 수 있습니다.
```
sudo arch -x86_64 gem install ffi
```
```
arch -x86_64 pod install
```

이 명령은 ffi 패키지를 설치하여 동적으로 연결된 라이브러리를 로드하고 포드 설치를 올바르게 실행할 수 있도록 하고 적절한 아키텍처로 포드 설치를 실행합니다.


## 1.4 샘플 RN 생성
홈으로 가서
```
cd ~
```
워크스페이스로 사용할 디렉토리 만들고
```
mkdir RN-workspace
```
```
cd RN-workspace
```
생성 (중간에 FoodDeliveryApp은 앱이름)
```
npx react-native init FoodDeliveryApp --template react-native-template-typescript
```
중간에 뭘로 인스톨할거냐고 물어봐서 homebrew로 하라고 했다


## 1.5 안드로이드 스튜디오

### 1.5.1 다운로드
> https://developer.android.com/studio?gclid=Cj0KCQjw-JyUBhCuARIsANUqQ_Ib7XxD35fEIXFQDl9C2_4SFUCIeTGwfkhb32zjp4boSSfnorFUqKkaAgTOEALw_wcB&gclsrc=aw.ds
>
> 아마 url이 나중엔 바뀔수도 있을느낌인데
> 그냥 구글에서 서칭해서 깔자 
> 나는 맥 인텔칩


### 1.5.2 import
> 프로젝트 open으로 FoodDeliveryApp을 열었다


### 1.5.3 SDK
> 나는 32버전 SDK를 설치했다.


### 1.5.4 그래들 설치
```
brew install gradle 
```


### 1.5.5 local.properties
> 참고 : https://eso0609.tistory.com/92
>
> 1. React Native 프로젝트에서 android 디렉토리로 접근한다.
> 2. android 디렉토리에서 local.properties 파일을 생성한다.
> 3. 아래 코드를 입력한다.
> sdk.dir = /Users/USERNAME/Library/Android/sdk


### 1.5.6 ANDROID_HOME

```
vi ~/.bash_profile
```

아래 내용을 추가

```
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

```
source ~/.bash_profile
```

이후에 안드로이드 스튜디오를 껐다켜자


### 1.5.7 가상기기 추가

나는 넥서스5로 했다.


### 1.5.8 실행

FoodDeliveryApp 디렉토리에서

```
npm run android
```


## 1.6 ios

### 1.6.1 아이폰용 라이브러리를 cocoapod통해서 설치
```
npx pod-install
```

오류났을때 지우는 방법은 ios디렉토리 들어가서
```
pod deintergrate
```

### 1.6.2 안드로이드 스튜디오에서 실행

```
npm rum ios
```

### 1.6.3 Xcode에서 실행

왼쪽위 재생버튼

