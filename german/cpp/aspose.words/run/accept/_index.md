---
title: "Aspose::Words::Run::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Run::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/run/accept/
---
## Run::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::Run::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der den Knoten besuchen wird. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Hinweise


Ruft [VisitRun()](../../documentvisitor/visitrun/) auf.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

## Siehe auch

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
