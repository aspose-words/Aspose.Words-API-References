---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes Methode"
linktitle: "GetChildNodes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes Methode. Gibt eine Live‑Sammlung von Kindknoten zurück, die dem angegebenen Typ in C++ entsprechen."
type: docs
weight: 34500
url: /de/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Gibt den Typ der auszuwählenden Knoten an. |
| isDeep | bool | **true** zum Auswählen aller Kindknoten rekursiv; **false** zum Auswählen nur der unmittelbaren Kinder. |

### ReturnValue

Eine Live‑Sammlung von Kindknoten des angegebenen Typs.
## Hinweise


Die von dieser Methode zurückgegebene Knotensammlung ist stets live.

Eine Live‑Sammlung ist stets mit dem Dokument synchronisiert. Zum Beispiel, wenn Sie alle Abschnitte in einem Dokument auswählen und die Sammlung durchlaufen, um die Abschnitte zu löschen, wird der Abschnitt sofort aus der Sammlung entfernt, sobald er aus dem Dokument entfernt wird.

## Siehe auch

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
