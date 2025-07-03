---
title: Aspose::Words::Markup::IStructuredDocumentTag::get_SdtType method
linktitle: get_SdtType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::get_SdtType method. Gets type of this Structured document tag in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.markup/istructureddocumenttag/get_sdttype/
---
## IStructuredDocumentTag::get_SdtType method


Gets type of this **Structured document tag**.

```cpp
virtual Aspose::Words::Markup::SdtType Aspose::Words::Markup::IStructuredDocumentTag::get_SdtType()=0
```


## Examples



Shows how to get the type of a structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSection, tags->idx_get(0)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSectionItem, tags->idx_get(1)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RichText, tags->idx_get(2)->get_SdtType());
```

## See Also

* Enum [SdtType](../../sdttype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
