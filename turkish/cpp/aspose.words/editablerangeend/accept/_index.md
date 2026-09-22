---
title: "Aspose::Words::EditableRangeEnd::Accept metodu"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRangeEnd::Accept metodu. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Açıklamalar


Çağırır [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/).

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
