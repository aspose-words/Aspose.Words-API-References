---
title: "طريقة Aspose::Words::SubDocument::get_NodeType"
linktitle: "get_NodeType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::SubDocument::get_NodeType. تُرجع SubDocument في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


تُرجع [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## أمثلة



يظهر كيفية الوصول إلى المستند الفرعي للوثيقة الرئيسية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// تعمل هذه العقدة كمرجع إلى مستند خارجي، ولا يمكن الوصول إلى محتوياتها.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## انظر أيضًا

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
