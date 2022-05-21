# 1. 개발 환경 구축 (Mac)

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


## 1.2 expo-cli 설치
```
npm install -g expo-cli
```
      

* 결과예시
```
sghahaucBookPro:~ sghaha$ npm install -g expo-cli
npm WARN deprecated source-map-url@0.4.1: See https://github.com/lydell/source-map-url#deprecated
npm WARN deprecated querystring@0.2.0: The querystring API is considered Legacy. new code should use the URLSearchParams API instead.
npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm WARN deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
npm WARN deprecated fsevents@1.2.13: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.
npm WARN deprecated fsevents@1.2.13: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.
npm WARN deprecated chokidar@2.1.8: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated chokidar@2.1.8: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated svgo@1.3.2: This SVGO version is no longer supported. Upgrade to v2.x.x.
npm WARN deprecated subscriptions-transport-ws@0.9.8: The `subscriptions-transport-ws` package is no longer maintained. We recommend you use `graphql-ws` instead. For help migrating Apollo software to `graphql-ws`, see https://www.apollographql.com/docs/apollo-server/data/subscriptions/#switching-from-subscriptions-transport-ws    For general help using `graphql-ws`, see https://github.com/enisdenjo/graphql-ws/blob/master/README.md
npm WARN deprecated graphql-tools@3.0.0: This package has been deprecated and now it only exports makeExecutableSchema.\nAnd it will no longer receive updates.\nWe recommend you to migrate to scoped packages such as @graphql-tools/schema, @graphql-tools/utils and etc.\nCheck out https://www.graphql-tools.com to learn what package you should use instead

added 1520 packages, and audited 1521 packages in 51s

120 packages are looking for funding
  run `npm fund` for details

25 vulnerabilities (12 moderate, 13 high)

To address issues that do not require attention, run:
  npm audit fix

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
npm notice 
npm notice New minor version of npm available! 8.3.1 -> 8.10.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v8.10.0
npm notice Run npm install -g npm@8.10.0 to update!
npm notice 
```



## 1.3 샘플 RN 생성
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
