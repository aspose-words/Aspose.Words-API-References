---
title: Aspose::Words::Markup::StructuredDocumentTag::get_SdtType method
linktitle: get_SdtType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_SdtType method. Gets type of this Structured document tag in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words.markup/structureddocumenttag/get_sdttype/
---
## StructuredDocumentTag::get_SdtType method


Gets type of this **Structured document tag**.

```cpp
Aspose::Words::Markup::SdtType Aspose::Words::Markup::StructuredDocumentTag::get_SdtType() override
```


## Examples



Shows how to get the type of a structured document tag. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Structured document tags.docx");

SharedPtr<System::Collections::Generic::List<SharedPtr<StructuredDocumentTag>>> sdTags =
    doc->GetChildNodes(NodeType::StructuredDocumentTag, true)->LINQ_OfType<SharedPtr<StructuredDocumentTag>>()->LINQ_ToList();

ASSERT_EQ(SdtType::RepeatingSection, sdTags->idx_get(0)->get_SdtType());
ASSERT_EQ(SdtType::RepeatingSectionItem, sdTags->idx_get(1)->get_SdtType());
ASSERT_EQ(SdtType::RichText, sdTags->idx_get(2)->get_SdtType());
```

## See Also

* Enum [SdtType](../../sdttype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
