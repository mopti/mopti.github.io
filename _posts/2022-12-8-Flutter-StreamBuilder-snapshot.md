## snapshot

### [1] snapshot
```
AsyncSnapshot<QuerySnapshot<Map<String, dynamic>>> snapshot
```

### [2] snapshot.data!
```
QuerySnapshot<Map<String, dynamic>> querySnapshot= snapshot.data!;
```

### [3] querySnapshot.docs
```
List<QueryDocumentSnapshot<Map<String, dynamic>>> queryDocumentSnapshot= querySnapshot.docs;
```

### [4] queryDocumentSnapshot // Map이 담긴 List 임
```
queryDocumentSnapshot[index]['key'] // 참조가능

for (var map in queryDocumentSnapshot)
{
	resultList.add(map);
}
```
