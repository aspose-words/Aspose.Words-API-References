---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::SdtAppearance enum. C++'ta yapılandırılmış belge etiketinin görünümünü belirtir."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Yapılandırılmış belge etiketinin görünümünü belirtir.

```cpp
enum class SdtAppearance
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| BoundingBox | 0 | Gölgelendirilmiş bir dikdörtgen veya sınırlama kutusu olarak gösterilen yapılandırılmış belge etiketini temsil eder. |
| Tags | 1 | Başlangıç ve bitiş işaretçileri olarak gösterilen yapılandırılmış belge etiketini temsil eder. |
| Gizli | 2 | Görünmeyen bir yapılandırılmış belge etiketini temsil eder. |
| Default | n/a | Varsayılan olarak [BoundingBox](./) kullanılır. |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
