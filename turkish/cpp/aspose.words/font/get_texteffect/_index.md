---
title: "Aspose::Words::Font::get_TextEffect yöntemi"
linktitle: "get_TextEffect"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_TextEffect yöntemi. C++'ta yazı tipi animasyon etkisini alır veya ayarlar."
type: docs
weight: 47000
url: /tr/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Yazı tipi animasyon etkisini alır veya ayarlar.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## Örnekler



Bir metin koşuluna görsel efekt uygulamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Microsoft Word'ün eski sürümleri yalnızca yazı tipi animasyon efektlerini destekler.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## Ayrıca Bakınız

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
