# 2022-11-14 Flutter

? 회사에서 React Native 를 공부하다 Flutter 얘기가 나와 알아보는 내용

---

1. 설치관련
 - 안드로이드 스튜디오를 설치해준다. (최신버전)
 - 공식 홈페이지에 접속한다.
 https://docs.flutter.dev/get-started/install/windows
 - git을 설치한다
 
 ![image](https://user-images.githubusercontent.com/96710610/201670460-13bb0087-038f-4e38-b61f-525f711ecdb4.png)
 
 ---
 
 - Flutter SDK 받기 하단에 알집을 다운받는다.
 - 다운받는 중간에 C 드라이브에 flutter 를 설치할 폴더를 하나 만들어준다. ( ex : C:\dev )
 - 폴더만든곳에 다운받은 알집을 푼다 
 
 ![image](https://user-images.githubusercontent.com/96710610/201670665-898d0012-d304-4604-8729-f8464a3e39b9.png)
 
 ---
 
 - 환경변수에 flutter를 추가해준다.

 ![image](https://user-images.githubusercontent.com/96710610/201670870-5bd3efa2-7f77-4ebf-94e7-5b946afcd1e9.png)
 
 ---
 
 - C:\dev\flutter 에 보면 flutter_console.bat 가 있다. 클릭해서 눌러준 후 flutter doctor 를 검색한다.

 ![image](https://user-images.githubusercontent.com/96710610/201671344-532dbc20-9046-45ad-9284-9db1fc0eee11.png)
 
 ---
 
 - 난 위와 같이 에러가 났기 때문에 해결을 해준다.

 ![image](https://user-images.githubusercontent.com/96710610/201673736-9b0657a1-1bf4-4b06-a234-3f7df6469167.png)
 
 ---
 
  1) 원인을 모르겠어서 검색을 한 결과 android studio 에 가서 위 이미지대로 설치했다
   - 자료 참고 (https://stackoverflow.com/questions/69110608/flutter-doctor-results-with-cmdline-tools-component-is-missing)
  2) Visual Studio Code 는 뭐가 문젠가 한참을 검색해봤는데 결국 내가 설치한 건 Windows, macOS 및 Linux에서 실행되는 독립 실행형 소스 코드 편집기 였고
  설치해야하는건 Windows에서 .NET 및 C++ 개발자를 위한 최고의 포괄적인 IDE 라고 써있는것이었다.
   - 다운로드 참고 (https://visualstudio.microsoft.com/ko/downloads/)

  ![image](https://user-images.githubusercontent.com/96710610/201686499-f340e5ab-5eeb-44df-ab3c-37153b4fac88.png)
  
  ---
  
  # 2022-11-17 Flutter
  
  Flutter 프로젝트 생성 방법
   
   ![image](https://user-images.githubusercontent.com/96710610/202463847-a8fe2128-bf7f-4d68-b0a8-1fb09d903fbd.png)
   
   ---
   
   - Visual Studio Code 내 Extensions 에 Flutter를 검색해서 설치해준다.
   
   ![image](https://user-images.githubusercontent.com/96710610/202466220-1eed4ecd-3ad4-4ff1-883b-5f19a0031d95.png)
   
   ---
   
   - ctrl + shift + p 혹은 상단 View > Command Palette.. 로 써있는것을 선택해준다.
   
   flutter New Project 를 누르고
   
   Application 를 선택한 후 저장위치를 선택하고 확인을 눌러준다.
   
   프로젝트 생성 
   
  # 2022-11-22 Flutter

  프로젝트 생성 중 아래와 같은 코드가 떴다.
   
   ```
   flutter create --template app --overwrite .
   Cannot create a project within the Flutter SDK. Target directory 'C:\dev\flutter\project\test05' is within the Flutter SDK at 'C:\dev\flutter'.
   exit code 2
   ```

 Flutter 프로젝트 실행 방법
 ctrl + shift + p 혹은 상단 View > Command Palette..을 클릭 후 >Flutter: Select Device 를 찾아 실행하면 디바이스가 실행된다.
 
 
 
   

 
