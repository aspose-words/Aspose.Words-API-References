---
title: "Aspose::Words::EditableRangeStart::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EditableRangeStart::Accept yöntemi. C++'da bir ziyaretçi kabul eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/editablerangestart/accept/
---
## EditableRangeStart::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::EditableRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Açıklamalar


Çağırır [VisitEditableRangeStart()](../../documentvisitor/visiteditablerangestart/).

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
