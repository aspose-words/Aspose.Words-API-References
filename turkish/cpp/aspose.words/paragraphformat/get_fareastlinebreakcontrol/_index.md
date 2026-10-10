---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl yöntemi"
linktitle: "get_FarEastLineBreakControl"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl yöntemi. Doğu Asya satır sonu kurallarının geçerli paragraf için uygulanıp uygulanmadığını gösteren bir bayrağı alır veya ayarlar C++'da."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Doğu Asya satır sonlandırma kurallarının geçerli paragraf için uygulanıp uygulanmadığını gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
```


## Örnekler



Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
