---
title: "Aspose::Words::Tables::Row::Accept метод"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Row::Accept метод. Принимает посетителя в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.tables/row/accept/
---
## Row::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::Tables::Row::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет обходить узлы. |

### ReturnValue

True, если все узлы были посещены; false, если [DocumentVisitor](../../../aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.
## Примечания


Перебирает этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод у [DocumentVisitor](../../../aspose.words/documentvisitor/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
