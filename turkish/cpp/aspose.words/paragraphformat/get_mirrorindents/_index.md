---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents yöntemi"
linktitle: "get_MirrorIndents"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_MirrorIndents yöntemi. Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bir bayrağı alır veya ayarlar (C++)."
type: docs
weight: 24500
url: /tr/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Örnekler



Sol ve sağ girintileri aynı hale getirmeyi göster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
