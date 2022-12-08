## snapshot data type

### [1] snapshot
```dart
AsyncSnapshot<QuerySnapshot<Map<String, dynamic>>> snapshot
```

### [2] snapshot.data!
```dart
QuerySnapshot<Map<String, dynamic>> querySnapshot= snapshot.data!;
```

### [3] querySnapshot.docs
```dart
List<QueryDocumentSnapshot<Map<String, dynamic>>> queryDocumentSnapshot= querySnapshot.docs;
```

### [4] queryDocumentSnapshot // Map이 담긴 List 임
```dart
queryDocumentSnapshot[index]['key'] // 참조가능

for (var map in queryDocumentSnapshot)
{
	resultList.add(map);
}
```
