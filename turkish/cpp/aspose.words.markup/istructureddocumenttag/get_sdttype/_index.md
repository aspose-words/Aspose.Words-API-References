---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_SdtType metodu"
linktitle: "get_SdtType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_SdtType metodu. C++'ta bu Yapılandırılmış belge etiketinin tipini alır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_sdttype/
---
## IStructuredDocumentTag::get_SdtType method


Bu **Structured document tag** tipini alır.

```cpp
virtual Aspose::Words::Markup::SdtType Aspose::Words::Markup::IStructuredDocumentTag::get_SdtType()=0
```


## Örnekler



Yapılandırılmış bir belge etiketinin tipini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSection, tags->idx_get(0)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSectionItem, tags->idx_get(1)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RichText, tags->idx_get(2)->get_SdtType());
```

## Ayrıca Bakınız

* Enum [SdtType](../../sdttype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
