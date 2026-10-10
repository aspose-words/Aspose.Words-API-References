---
title: "Aspose::Words::ParagraphFormat::get_BaselineAlignment method"
linktitle: "get_BaselineAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_BaselineAlignment method. C++'ta bir satırdaki yazı tiplerinin dikey konumunu alır veya ayarlar."
type: docs
weight: 5500
url: /tr/cpp/aspose.words/paragraphformat/get_baselinealignment/
---
## ParagraphFormat::get_BaselineAlignment method


Bir satırdaki yazı tiplerinin dikey konumunu alır veya ayarlar.

```cpp
Aspose::Words::BaselineAlignment Aspose::Words::ParagraphFormat::get_BaselineAlignment()
```


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

* Enum [BaselineAlignment](../../baselinealignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
