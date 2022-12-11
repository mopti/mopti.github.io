## Problem
- Http Package를 사용한 app을 apk로 build한 후 핸드폰에서 실행하면 통신이 되지 않는 문제 발생.

## Solution
```dart
<manifest xmlns:android...>
 ...
 <uses-permission android:name="android.permission.INTERNET" />
 <application ...
</manifest>
```
- AndroidManifest.xml 파일에서 인터넷 사용 설정을 해줘야 함.
- 참고 : https://docs.flutter.dev/development/data-and-backend/networking