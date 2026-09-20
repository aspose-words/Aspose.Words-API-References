---
title: "Метод Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes"
linktitle: "GetChildNodes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes. Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу, в C++."
type: docs
weight: 34500
url: /ru/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Указывает тип узлов для выбора. |
| isDeep | bool | **true** — выбрать из всех дочерних узлов рекурсивно; **false** — выбрать только среди непосредственных дочерних узлов. |

### ReturnValue

Живая коллекция дочерних узлов указанного типа.
## Примечания


Коллекция узлов, возвращаемая этим методом, всегда живая.

Живая коллекция всегда синхронизирована с документом. Например, если вы выбрали все разделы в документе и перебираете коллекцию, удаляя разделы, раздел удаляется из коллекции сразу же, когда он удаляется из документа.

## См. также

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
