---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes metod"
linktitle: "GetChildNodes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes metod. Returnerar en levande samling av undernoder som matchar den angivna typen i C++."
type: docs
weight: 34500
url: /sv/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Returnerar en dynamisk samling av barnnoder som matchar den angivna typen.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Anger typen av noder som ska väljas. |
| isDeep | bool | **true** för att välja från alla barnnoder rekursivt; **false** för att endast välja bland omedelbara barn. |

### ReturnValue

En levande samling av barnnoder av den angivna typen.
## Anmärkningar


Samlingen av noder som returneras av den här metoden är alltid levande.

En levande samling är alltid i synk med dokumentet. Till exempel, om du markerade alla sektioner i ett dokument och itererade genom samlingen och raderade sektionerna, tas sektionen bort från samlingen omedelbart när den tas bort från dokumentet.

## Se även

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
