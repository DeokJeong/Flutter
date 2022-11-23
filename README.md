  # 2022-11-14 Flutter

  ? 회사에서 React Native 를 공부하다 Flutter 얘기가 나와 알아보는 내용

  ---
  <h2>1. 설치관련</h2>

  
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
  
  
  <h2>2. Flutter 프로젝트 생성 방법</h2>
 
   
   ![image](https://user-images.githubusercontent.com/96710610/202463847-a8fe2128-bf7f-4d68-b0a8-1fb09d903fbd.png)
   
   ---
   
   - Visual Studio Code 내 Extensions 에 Flutter를 검색해서 설치해준다.
   
   ![image](https://user-images.githubusercontent.com/96710610/202466220-1eed4ecd-3ad4-4ff1-883b-5f19a0031d95.png)
   
   ---
   
   - ctrl + shift + p 혹은 상단 View > Command Palette.. 로 써있는것을 선택해준다.
   
   - flutter New Project 를 누르고 Application 를 선택한 후 저장위치를 선택하고 확인을 눌러준다.
   
   프로젝트 생성 
   
  # 2022-11-22 Flutter

  - 프로젝트 생성 중 아래와 같은 코드가 떴다.
   
   ```
   flutter create --template app --overwrite .
   Waiting for another flutter command to release the startup lock...
   Cannot create a project within the Flutter SDK. Target directory 'C:\dev\flutter\project\test04' is within the Flutter SDK at 'C:\dev\flutter'.
   exit code 2
   ```
   
   - 여러가지로 검색해본 결과 나의 실수라는것을 깨닳았다.

   - 나는 어디에 저장해야할지 몰라 바로 뜨는곳에 저장을 해버렸다.
   
   ![image](https://user-images.githubusercontent.com/96710610/203317077-dba1b67b-e97e-4d8a-b853-30830e251968.png)
   
   ---
   
   - 다시 프로젝트 저장 할 폴더를 만들고 그곳에 가서 프로젝트를 다시 생성하면 위와 같은 이미지가 뜬다.
   
   ![image](https://user-images.githubusercontent.com/96710610/203316041-ed0db226-6102-49f9-b31e-6ccd0dcf5d23.png)
   
   ---

   - 혹시 나와 같은 상황이 아닌데 같은 문구가 뜬다면 해당 이미지처럼 작업관리자에 가서 dart를 작업종료해준다.


  <h2>3. Flutter 프로젝트 실행 방법</h2>
 

   - 위 방식대로 프로젝트가 만들어졌다면 실행을 해본다. 
   
   - ctrl + shift + p 혹은 상단 View > Command Palette..을 클릭 후 >Flutter: Select Device 를 찾아 실행하면 디바이스가 실행된다.

   - 디바이스가 실행됬으면 프로젝트를 띄워주면된다 VS CODE 기준 Ctrl+F5 를 누르고 디버그 콘솔이 뜨면 main.dart를 치고 기다리면 프로젝트가 뜬다.


   ![image](https://user-images.githubusercontent.com/96710610/203320687-c0d88c3a-6b6b-40c8-a940-2187dcb4de80.png)
   
   ---

  # 2022-11-23 Flutter
  
  <h2> 4. Dart에 대한 이해 </h2>
  
  - Flutter를 이해하기전에 Dart를 이해하고 가면 더 쉽다는 얘기를 들었다.

  - 기존의 script와 비슷한 내용이지만 다시한번 이해를 해보고자 한다.

  ```
  void main() {
   print('hello code Fectory!');

   var name = '코드 팩토리';
   print(name);

   var name2 = 'Dart Test';
   print(name2);

   name = '플러터 프로그래밍';
   print(name);

   var name3 = '코드팩토리2';
   print(name3);
  }
  ```
    
    
  - 위와 같이 코드를 적었을경우 코드는 아래 콘솔과 같이 뜬다.
 
  ![image](https://user-images.githubusercontent.com/96710610/203542060-fec64138-c78d-4fd2-af76-866d3c35ada1.png)

  ---
    
  - 정수 integer
    
    ```
    void main() {
     // 정수
     // integer

     int number1 = 10;
     print(number1);

     int number2 = 15;
     print(number2);

     int number3 = -20;
     print(number3);
    }
    ```
    
  ![image](https://user-images.githubusercontent.com/96710610/203542527-56653ec7-189e-4a63-a1be-1c7668c74972.png)

  ---
    
  ```
 void main() {
   int number1 = 2;
   int number2 = 4;

   print(number1 + number2);
   print(number1 - number2);
   print(number1 / number2);
   print(number1 * number2);
  }
  ```
    
  ![image](https://user-images.githubusercontent.com/96710610/203542748-ee7394d3-6f90-48b5-a39a-421e19c42473.png)

  ---
    
  - 실수를 입력할때는 int 가 아닌 double을 써야한다고 한다. 만약 정수를 넣게되면 어떻게 될까 궁금해서 넣어봤다.
  - 하지만 아래와 같이 에러가 뜨고 말았다. 이로서 알게된건 맞지않은것에 대한 에러는 표현이 잘 되어있다는 점인것 같다.
      
  ```
  void main() {
   //실수
    //double

    double number1 = 2.5;
    print(number1);
    int number2 = 3.2;
    print(number2);
  }
  ```
    
  ![image](https://user-images.githubusercontent.com/96710610/203543090-9e0c052d-17a6-4efe-bfff-824e550028a2.png)

  ---
    
  - var로 쓰는것도 좋지만 명시를 해주는게 더 좋을 수 있다. Type을 알고싶을때 사용하는것은 runtimeType

  ```
  void main() {
  // 맞다 / 틀리다
  // boolean

  bool isTrue = true;
  bool isFalse = false;

  print(isTrue);
  print(isFalse);

  //글자
  // String

  String name = '코드팩토리';
  String name2 = 'Dart';

  print(name);
  print(name2);

  //var String

  var name3 = '다트 공부';
  var number = 20;

  print(name3.runtimeType);
  print(number.runtimeType);

  }

  ```
    
  ![image](https://user-images.githubusercontent.com/96710610/203572177-0f6d6f72-1f94-4da8-bb9b-7f7851ffcfac.png)


  ---
    
  - String 사이에 간격주는 방법 
  - ${} 괄호 안에 묶지않으면 코드로 인식 할 수 없다.

  ```
  void main() {

  String name = '비비';
  String name2 = '덕정';

  print(name + name2);
  print(name + ' ' + name2);

  print('${name} ${name2}');

  print('$name.runtimeType $name2');

  }

  ```
  
  ![image](https://user-images.githubusercontent.com/96710610/203573193-cd17f10a-87ce-4bd8-849d-2af0f1352329.png)

  ---
  
  - dynamic type은 어떤 타입이던 다 넣을 수 있음
  
  ```
    dynamic name = '다트학습';
  
  print(name);
  
  dynamic number = 1;
  
  var name2 = 'DartPad';
  
  print(name2);
  print(name.runtimeType);
  print(name2.runtimeType);
   
  ```
  ![image](https://user-images.githubusercontent.com/96710610/203573910-d1d9156e-ddb4-4084-baf1-c252fe203091.png)

  ---
  
  - 만일 dynamic 의 변수를 다른 타입의 변수로 변경한다면 변경이 가능하나 var 로 변수를 설정하면 초기 설정타입으로 픽스가 된다.

  ```
  void main() {
    dynamic name = '다트학습';

    var name2 = 'DartPad';

    name = 2;

    name2 = 3;
  } 
  ```
  
  ![image](https://user-images.githubusercontent.com/96710610/203574437-db6d2c51-3b7f-48c8-9ba1-4d4594150522.png)


  ---
  
  
    
    
