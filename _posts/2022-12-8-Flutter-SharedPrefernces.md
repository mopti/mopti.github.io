## Installation

```dart
flutter pub add shared_preferences

import 'package:shared_preferences/shared_preferences.dart';
```
https://pub.dev/packages/shared_preferences

## Usage
- 키-값 방식으로 데이터를 저장하는 방법 임. 기기 내 xml 파일에 간단한 정보를 저장하는 것임.
- 저장해야 하는 데이터 양이 적거나 아주 간단한 경우 사용할 수 있는 기법임
- 앱을 껐다 켜도 데이터가 유지 되는 것이 특징임. 주로 자동로그인이나 도움말 스킵여부를 결정하는데 사용 됨.


#### getBool
```dart
// (Method) shared_prefs로부터 'isLogin'값 읽기  
Future<bool> checkLogin() async {  
  // [shared_Prefs] 기기내 정보를 가져와 인스턴스 생성  
  SharedPreferences prefs = await SharedPreferences.getInstance();  
  
  // [shared_Prefs] isLogin 값 읽기
  // null 이면 => false 리턴  
  // null 이 아니면 => 그 결과값 리턴  
  bool isLogin = prefs.getBool('isLogin') ?? false;  
  debugPrint('[*] isLogin : $isLogin');  
  return isLogin;  
}
```

#### setBool
```dart
// (Method) shared_prefs에 'isLogin'값 쓰기
Future setLogin() async {  
  // [shared_prefs] 인스턴스 생성  
  SharedPreferences prefs = await SharedPreferences.getInstance();  
  // [shared_prefs] isLogin 값 쓰기  
  prefs.setBool('isLogin', true);  
}
```
