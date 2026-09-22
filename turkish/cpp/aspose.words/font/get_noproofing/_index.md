---
title: "Aspose::Words::Font::get_NoProofing metodu"
linktitle: "get_NoProofing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_NoProofing metodu. C++'da biçimlendirilmiş karakterlerin imla denetiminden geçirilmemesi gerektiğinde doğru."
type: docs
weight: 30000
url: /tr/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


Biçimlendirilmiş karakterlerin imla denetimi yapılmaması gerektiğinde doğrudur.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Örnekler



Microsoft Word tarafından metnin imla denetiminden nasıl korunacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normalde, Microsoft Word yazım hatalarını kırmızı, kesik alt çizgiyle vurgular.
// \"NoProofing\" bayrağını kaldırarak bir metin bölümü oluşturabiliriz ki
// imla denetimini atlar ve aynı zamanda tamamen devre dışı bırakır.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
