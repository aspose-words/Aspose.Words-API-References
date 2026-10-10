---
title: "Aspose::Words::Font::get_Kerning metodu"
linktitle: "get_Kerning"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Kerning metodu. C++'da kerning'in başladığı yazı tipi boyutunu alır veya ayarlar."
type: docs
weight: 20000
url: /tr/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Kerning'in başladığı yazı tipi boyutunu alır veya ayarlar.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Örnekler



Kerning'in etkili olmaya başladığı yazı tipi boyutunu nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Builder'ın yazı tipi boyutunu ve kerning'in etkili olacağı minimum boyutu ayarlayın.
// Yazı tipi boyutu kerning eşiğinin altına düştüğü için, aşağıdaki run kerning içermeyecek.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Kerning eşiğini, builder'ın mevcut yazı tipi boyutu onun üzerinde olacak şekilde ayarlayın.
// Bu noktadan itibaren eklediğimiz tüm metin kerning uygulanmış olacaktır. Karakterler arasındaki boşluklar
// ayarlanacak, genellikle biraz daha estetik açıdan hoş bir text run ortaya çıkar.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
