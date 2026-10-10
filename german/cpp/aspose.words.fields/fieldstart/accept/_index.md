---
title: "Aspose::Words::Fields::FieldStart::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldStart::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der den Knoten besuchen wird. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Hinweise


Ruft [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/) auf.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

## Siehe auch

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
