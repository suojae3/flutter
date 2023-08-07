
![header](https://capsule-render.vercel.app/api?type=waving&color=timeGradient&height=300&section=header&fontSize=35&text=Flutter%20The%20Complete%20Guide&animation=fadeIn&fontAlignY=42&fontAlign=30)

<br/>

---

## 목차

- [Ch01. Flutter Basic](#ch01-flutter-Basic) <br/>
- [Ch02. Debugging Flutter](#ch02-Debugging-flutter) <br/>
- [Ch03. Flutter State Basic](#ch03-flutter-state-basic) <br/>
- [Ch04. Flutter Architecture](#ch04-flutter-architecture) <br/>

<br/>

---

## Ch01. Flutter Basic

### 01. Widget 이란 무엇인가요?

- Widget은 Flutter UI의 가장 기본적인 단위로 간단한 블록부터 텍스트입력창, 특정 요소 간격조차 Widget으로 관리됩니다.
- Flutter 개발자의 필수 요구사항으로 이러한 Widget을 얼마나 적재적소에 효과적으로 활용할 수 있느냐 입니다. <br/><br/>

#

### 02. Widget Tree란 무엇인가요?

- Flutter Widget은 마치 블록과 같습니다. 어떻게 조합하느냐에 따라 전혀 다른 UI를 나오기도 하고 재사용하기도 합니다
- 이 때, Widget은 수평적,수직적인 관계가 만들어지는데 이런 관계를 나타낸 형태를 Widget tree 라고 부르며 추후 상태 관리하는 데 있어 중요한 개념입니다<br/><br/>

#

### 03.  import는 어떤용도인가요?

- 현재 사용하고 있는 다트 파일 외에 다른 다트 파일을 쓰기 위해서 가장 먼저 import를 선언해줍니다<br/><br/>

#

### 04. `Scaffold()`란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled.png" width="400" height="200"><br/><br/>

- 위젯 트리 최상위에 위치하는 `MaterialApp()`에서 화면을 구성하는 가장 기본적인 도화지 역할을 수행합니다
- 이러한 `Scaffold()` 는 기본화면을 가장 쉽게만들 수 있는 방법 중 하나입니다<br/><br/>

#

### 05. Hot restart 와 Hot reload 의 차이점은 무엇인가요?

- **Hot restart**는 앱을 재시작하는 형태입니다 이 기능을 활용하면 앱의 모든 상태가 초기화되고 변경사항을 반영합니다
- **Hot reload**는 앱을 재실행하지는 않지만 코드의 변경사항을 반영합니다. 이를 통해 앱의 상태를 유지한채로 수정사항을 확인하여 더욱 빠른 개발을 할 수 있습니다<br/><br/>

#

### 06. Hot restart/Hot reload 사용시 주의사항에 대해서 알려주세요

- 둘 모두 앱을 재 컴파일 후 빌드하는 것이 아니기 때문에 앱의 기초가 되는 네이티브 코드 수정이나, 라이브러리, Asset의 추가등 상황에서는 정상적으로 작동하지 ㅇ낳습니다
- 또한 지나치게 많은 변경사항이 있거나 추후 상태 관리 개발 단계에 도달하면 해당 기능 사용에 주의를 요합니다<br/><br/>

#

### 07.  Material Design 과 Cupertino Design 에 대해서 설명해주세요

- Flutter 내에서는 대표적인 2개의 디자인 가이드를 활용하여 개발할 수 있습니다(물론 커스텀 디자인도 가능)
- 구글 철학이 녹아져 있는 디자인 가이드는 Material Design, Apple의 철학이 녹아져 있는 디자인 가이드는 Cupertino Design이라고 구분짓고 있습니다
- 해당 디자인 가이드를 디바이스에 따라 분리 구현할 수도 있습니다<br/><br/>

#

### 08. `Container()` 에 대해서 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 1.png" width="400" height="200"><br/><br/>

- `Container()` 는 가장 기본적인 위젯 중 하나입니다
- `Container()`는 `child`를 통해서 내부에 들어갈 위젯을 선언하게 됩니다
- Container는 기본적으로 width와 height값을 가질 수 있습니다<br/><br/>

#

### 09. padding 과 margin 에 대해 설명해주세요

&nbsp;&nbsp;&nbsp;&nbsp;<img src="Untitled 2.png" width="400" height="200"><br/><br/>

- Padding은 위젯외곽선과 내부 컨텍스트의 간격을 넓혀주는 값이고 주로 `EdgeInsets.formLTRP` 나 `EdgeInsets.symmetric` 을 통해 주로 구현합니다
- Margin은 패딩과 반대로 외부 경계선과 밖의 간격을 설정해주는 값으로 패딩과 마찬가지로 `formLTRP`, `symmetric` 을 통해 주고 구현합니다.<br/><br/>

#

#### 10. 다트 파일은 어떻게 컴파일 과정을 거쳐서 Android / iOS 기기에서 작동되나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/1.png" width="400" height="200"><br/><br/>

- 먼저 Dart 파일이 처음 부터 끝까지 분석(Parse)됩니다
- Parse가 끝나면 flutter tool에 의해 타겟 플랫폼의 네이티브 언어로 번역됩니다.
- 이러한 네이티브 코드로 타켓 플랫폼의 기기에서 실행됩니다. 




---

## Ch02. Debugging Flutter


