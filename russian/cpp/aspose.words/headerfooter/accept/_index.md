---
title: "метод Aspose::Words::HeaderFooter::Accept"
linktitle: "Принять"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::HeaderFooter::Accept. Принимает посетителя в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/headerfooter/accept/
---
## HeaderFooter::Accept method


Принимает посетителя.

```cpp
bool Aspose::Words::HeaderFooter::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| посетитель | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Посетитель, который будет обходить узлы. |

### ReturnValue

True, если все узлы были посещены; false, если [DocumentVisitor](../../documentvisitor/) остановил операцию до посещения всех узлов.
## Примечания


Перебирает этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод у [DocumentVisitor](../../documentvisitor/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

## См. также

* Class [DocumentVisitor](../../documentvisitor/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
