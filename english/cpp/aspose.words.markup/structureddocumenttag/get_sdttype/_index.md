---
title: Aspose::Words::Markup::StructuredDocumentTag::get_SdtType method
linktitle: get_SdtType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_SdtType method. Gets type of this Structured document tag in C++.'
type: docs
weight: 84000
url: /cpp/aspose.words.markup/structureddocumenttag/get_sdttype/
---
## StructuredDocumentTag::get_SdtType method


Gets type of this Structured document tag.

```cpp
Aspose::Words::Markup::SdtType Aspose::Words::Markup::StructuredDocumentTag::get_SdtType() override
```

## Examples


Shows how to get the type of a structured document tag.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Structured document tags.docx"));

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>()->LINQ_ToList();

ASSERT_EQ(tags->idx_get(0)->get_SdtType(), SdtType::RepeatingSection);
ASSERT_EQ(tags->idx_get(1)->get_SdtType(), SdtType::RepeatingSectionItem);
ASSERT_EQ(tags->idx_get(2)->get_SdtType(), SdtType::RichText);
```
## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
