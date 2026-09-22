---
title: "Aspose::Words::ParagraphFormat::get_WordWrap yöntemi"
linktitle: "get_WordWrap"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_WordWrap yöntemi. Bu özellik false ise, kelimenin ortasındaki Latin metni mevcut paragrafta kaydırılabilir. Aksi takdirde Latin metin C++'ta tam kelimelerle kaydırılır."
type: docs
weight: 42000
url: /tr/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Bu özellik **false** ise, kelimenin ortasındaki Latin metni geçerli paragrafta kaydırılabilir. Aksi takdirde Latin metni bütün kelimeler halinde kaydırılır.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
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
