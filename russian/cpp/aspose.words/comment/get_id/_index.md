---
title: "Метод Aspose::Words::Comment::get_Id"
linktitle: "get_Id"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comment::get_Id. Получает или задаёт идентификатор комментария в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Получает или задает идентификатор комментария.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Примечания


Идентификатор комментария позволяет привязать комментарий к области текста в документе. Область должна быть обозначена с помощью объектов [CommentRangeStart](../../commentrangestart/) и [CommentRangeEnd](../../commentrangeend/), использующих то же значение идентификатора, что и объект [Comment](../).

Это значение следует использовать при поиске узлов [CommentRangeStart](../../commentrangestart/) и [CommentRangeEnd](../../commentrangeend/), связанных с этим комментарием.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## См. также

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
