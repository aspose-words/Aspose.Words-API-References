---
title: "Aspose::Words::BaselineAlignment enum"
linktitle: "BaselineAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BaselineAlignment enum. Bir satırdaki yazı tiplerinin dikey konumunu C++'ta belirtir."
type: docs
weight: 80500
url: /tr/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Bir satırdaki yazı tiplerinin dikey konumunu belirtir.

```cpp
enum class BaselineAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Üst | 0 | Her bir yazı tipinin üst kısmına hizalar. |
| Orta | 1 | Her bir yazı tipinin merkez noktalarını hizalar. |
| Taban Çizgisi | 2 | Paragrafın taban çizgisine hizalar. |
| Alt | 3 | Her bir yazı tipinin alt kısmına hizalar. |
| Otomatik | 4 | Taban çizgisi otomatik olarak ayarlanır. |


## Örnekler



Bir satırdaki yazı tiplerinin dikey konumunun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
