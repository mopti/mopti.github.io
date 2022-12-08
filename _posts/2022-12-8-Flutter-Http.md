## Installation

```dart
flutter pub add http

import 'package:http/http.dart' as http;
```



## Usage


#### 1. http.Client 인스턴스 생성
```dart
static var client = http.Client();
```

#### 2. Url 설정 후 데이터 받기
```dart
String url = '...';  

var response = await client.get(Uri.parse(url));
```

#### 3. 연결성공여부 점검
```dart
if (response.statusCode == 200) {

} else {

}
```

#### 4. 받은 데이터 사용
```dart
String jsonString = response.body;  // String
List<dynamic> jsonDataList = jsonDecode(jsonString); // List
```

## Example
```dart
class APIMOCKAROO {  
  // [http] 인스턴스 생성, ulr 설정  
  final _client = http.Client();  
  final String _url = '...';  
  
  Future<List<dynamic>?> fetchMockarooData() async {  
    try {  
      // [http] Url 로 부터 response 받기  
      http.Response response = await _client.get(Uri.parse(_url));  
  
      // 전송 성공시  
      if (response.statusCode == 200) {  
        // => body 내용 디코딩 후 List에 저장  
        String jsonString = response.body;  
        List<dynamic> jsonDataList = jsonDecode(jsonString);  
  
        // => List 반환  
        return jsonDataList; // Map  
      }  
      // 전송 실패시  
      else {  

      }  
    } catch (e) {  

      return null;  
    }  
  }  
}
```