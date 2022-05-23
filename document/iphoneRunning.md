# 2. 아이폰에서 RN 돌려보기(Mac)

Xcode에서 시뮬레이터로 테스트하기 답답하니 아이폰 디바이스에 올려서 테스트 해보자

## 2.1 개발자 생성
개발자 등록이 아닌 계정을 생성하는 것이라 무료다.    
이미 개발자를 생성하였다면 넘어가도된다.

1. 애플 개발자 페이지 이동   
https://developer.apple.com/

2. 오른쪽 위에 Accout 클릭

3. 애플 계정으로 로그인

4. 약관 동의
By checking this box I confirm that I have read and agree to be bound by the Agreement above.    
를 눌러 동의하고 Submit


## 2.2 디바이스 테스트

### 2.2.1 Signing & Capabilities

1. USB로 아이폰과 Mac을 연결

2. Xcode 실행

3. Signing & Capabilities 선택 (General 탭 옆)

4. Signing 섹션. Team 항목 옆에 Add an Account 클릭

5. 애플 개발자 계정의 id/pw 입력하고 Next

6. Download Manual Profiles를 눌러 다운로드 

7. 창 닫는다.

8. 이제 Team에 드롭다운 생겼을 것임

9. 아까 추가한 아이디 선택

### 2.2.2 target

1. 왼쪽 Target 섹션에

2. 앱이름Tests 선택

3. Team옆에 드롭다운 메뉴를 선택하여 signing 선택

4. 맨위에 디바이스 선택하는거에서 나의 Device를 선택

5. 실행버튼

6. 앱이 깔리면 신뢰할수 없다고 할텐데

7. 핸드폰 설정 - 일반 - 기기관리 - 애플 개발자 계정(Apple 
developer account)을 선택하고 신뢰함 클릭
