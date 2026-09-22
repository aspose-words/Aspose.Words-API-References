---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextEffect enum. C++'de metin akışları için animasyon etkisi."
type: docs
weight: 123000
url: /tr/cpp/aspose.words/texteffect/
---
## TextEffect enum


Metin çalıştırmaları için animasyon efekti.

```cpp
enum class TextEffect
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
