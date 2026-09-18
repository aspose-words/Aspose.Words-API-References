---
title: "Aspose::Words::Document::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/document/accept/
---
## Document::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::Document::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der die Knoten besuchen wird. |

### ReturnValue

Wahr, wenn alle Knoten besucht wurden; falsch, wenn [DocumentVisitor](../../documentvisitor/) die Operation gestoppt hat, bevor alle Knoten besucht wurden.
## Hinweise


Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft die entsprechende Methode auf [DocumentVisitor](../../documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

## Siehe auch

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
