---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::EmphasisMark enum. C++'da vurgulama işareti için olası tipleri belirtir."
type: docs
weight: 89000
url: /tr/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Vurgu işaretinin olası türlerini belirtir.

```cpp
enum class EmphasisMark
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Vurgulama işareti yok. |
| OverSolidCircle | 1 | Vurgulama işareti, metnin üzerinde gösterilen katı siyah bir dairedir. |
| OverComma | 2 | Vurgulama işareti, metnin üzerinde gösterilen bir virgül karakteridir. |
| OverWhiteCircle | 3 | Vurgulama işareti, metnin üzerinde gösterilen boş beyaz bir dairedir. |
| UnderSolidCircle | 4 | Vurgulama işareti, metnin altında gösterilen katı siyah bir dairedir. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
