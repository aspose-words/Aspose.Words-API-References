---
title: "Aspose::Words::Notes::FootnoteSeparator::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteSeparator::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.notes/footnoteseparator/accept/
---
## FootnoteSeparator::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::Notes::FootnoteSeparator::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der die Knoten besuchen wird. |

### ReturnValue

Wahr, wenn alle Knoten besucht wurden; falsch, wenn [DocumentVisitor](../../../aspose.words/documentvisitor/) die Operation gestoppt hat, bevor alle Knoten besucht wurden.
## Hinweise


Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft die entsprechende Methode auf [DocumentVisitor](../../../aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

## Siehe auch

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FootnoteSeparator](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
