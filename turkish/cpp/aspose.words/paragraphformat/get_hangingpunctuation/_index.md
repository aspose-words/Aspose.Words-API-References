---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation yöntemi"
linktitle: "get_HangingPunctuation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation yöntemi. C++ içinde mevcut paragrafta sarkan noktalama işaretlerinin etkin olup olmadığını gösteren bir bayrağı alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Geçerli paragrafta sarkıt noktalama işaretlerinin etkin olup olmadığını gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
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
