---
title: Mongoose 의 예약 스키마
---

회사 팀 스터디에서 *Mongoose* 를 사용해서 디비 작업을 하는데

field 명을 `modelName` 으로 했더니 오류가 났다.

```
'modelName' may not be used as a schema pathname
```

그래서 검색을 해보니 `modelName` 이 *Mongoose* 의 예약 스키마 였다.

*Mongoose* 의 예약 스키마들

```
on, emit, _events, db, get, set, init, isNew, errors, schema, options, modelName, collection, _pres, _posts, toObject

```

[참조 doc](http://mongoosejs.com/docs/api.html#schema_Schema.reserved)
