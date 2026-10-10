---
title: "Aspose::Words::SubDocument::get_NodeType metodu"
linktitle: "get_NodeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SubDocument::get_NodeType metodu. C++'de SubDocument döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Döndürür [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Örnekler



Ana belgenin alt belgesine nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Bu düğüm dış bir belgeye referans olarak hizmet eder ve içeriğine erişilemez.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## Ayrıca Bakınız

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
