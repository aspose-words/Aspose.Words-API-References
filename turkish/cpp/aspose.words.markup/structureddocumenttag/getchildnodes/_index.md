---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes yöntemi"
linktitle: "GetChildNodes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes yöntemi. C++'ta belirtilen türe uyan alt düğümlerin canlı bir koleksiyonunu döndürür."
type: docs
weight: 34500
url: /tr/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Seçilecek düğüm tipini belirtir. |
| isDeep | bool | **true** tüm alt düğümlerden özyinelemeli olarak seçmek için; **false** yalnızca doğrudan alt düğümler arasında seçmek için. |

### ReturnValue

Belirtilen tipteki alt düğümlerin canlı bir koleksiyonu.
## Açıklamalar


Bu yöntem tarafından döndürülen düğüm koleksiyonu her zaman canlıdır.

Canlı bir koleksiyon her zaman belgeyle senkronizedir. Örneğin, bir belgede tüm bölümleri seçip koleksiyonu döngüyle gezerek bölümleri silerseniz, bölüm belge üzerinden kaldırıldığında koleksiyondan da hemen kaldırılır.

## Ayrıca Bakınız

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
