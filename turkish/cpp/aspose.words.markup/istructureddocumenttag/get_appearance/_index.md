---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance method"
linktitle: "get_Appearance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance method. C++'da yapılandırılmış belge etiketinin görünümünü alır veya ayarlar."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_appearance/
---
## IStructuredDocumentTag::get_Appearance method


Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar.

```cpp
virtual Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance()=0
```


## Örnekler



İçeriğin etrafında etiketi nasıl göstereceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Ayrıca Bakınız

* Enum [SdtAppearance](../../sdtappearance/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
