---
title: "Aspose::Words::BookmarkEnd::Accept метод"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BookmarkEnd::Accept метод. Принимает посетителя в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/bookmarkend/accept/
---
## BookmarkEnd::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::BookmarkEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет посещать узел. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Примечания


Вызывает [VisitBookmarkEnd()](../../documentvisitor/visitbookmarkend/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
