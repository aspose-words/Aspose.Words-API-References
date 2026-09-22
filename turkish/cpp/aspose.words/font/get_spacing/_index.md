---
title: "Aspose::Words::Font::get_Spacing yöntemi"
linktitle: "get_Spacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Spacing yöntemi. Karakterler arasındaki boşluğu (nokta cinsinden) C++'de döndürür veya ayarlar."
type: docs
weight: 40000
url: /tr/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


Karakterler arasındaki boşluğu (puan cinsinden) döndürür veya ayarlar.

```cpp
double Aspose::Words::Font::get_Spacing()
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
