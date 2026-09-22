---
title: "Aspose::Words::Font::get_EmphasisMark yöntemi"
linktitle: "get_EmphasisMark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_EmphasisMark yöntemi. C++ içinde bu biçimlendirmeye uygulanan vurgu işaretini alır veya ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Bu biçimlendirmeye uygulanan vurgu işaretini alır veya ayarlar.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Örnekler



Bir glif karakterinin üstüne/altına ek karakter nasıl eklenir gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Vurgulama işareti için olası tipler:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Ayrıca Bakınız

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
