---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance metodu"
linktitle: "get_Appearance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance metodu. C++'ta yapılandırılmış belge etiketinin görünümünü alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_appearance/
---
## StructuredDocumentTagRangeStart::get_Appearance method


Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar.

```cpp
Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance() override
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
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
