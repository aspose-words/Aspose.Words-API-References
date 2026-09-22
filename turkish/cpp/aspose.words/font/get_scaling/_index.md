---
title: "Aspose::Words::Font::get_Scaling yöntemi"
linktitle: "get_Scaling"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Scaling yöntemi. C++'da karakter genişliği ölçeklemesini yüzde olarak alır veya ayarlar."
type: docs
weight: 33000
url: /tr/cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Karakter genişliği ölçeklendirmesini yüzde olarak alır veya ayarlar.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
```


## Örnekler



Karakterler için yatay ölçekleme ve boşluk ayarlamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Metin akışı ekleyin ve karakter genişliğini %150'ye artırın.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Metin akışı ekleyin ve her karakter arasında 1pt ekstra yatay boşluk ekleyin.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Metin akışı ekleyin ve karakterleri 1pt daha yakınlaştırın.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
