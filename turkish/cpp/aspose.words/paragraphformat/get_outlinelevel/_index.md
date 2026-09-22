---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel metodu"
linktitle: "get_OutlineLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel metodu. C++'ta belgede paragrafın anahat seviyesini belirtir."
type: docs
weight: 26000
url: /tr/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Belgedeki paragrafın anahat seviyesini belirtir.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Örnekler



Paragraf taslak seviyelerini yapılandırarak katlanabilir metin oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Her paragrafın bir OutlineLevel'ı vardır; bu, 1 ile 9 arasında herhangi bir sayı olabilir veya varsayılan "BodyText" değerinde olabilir.
// Özelliği numaralı değerlerden birine ayarlamak, sola bir ok gösterecektir
// paragrafın başlangıcının solunda.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Seviye 1 en üst seviyedir. Daha yüksek bir seviyenin altında daha düşük seviyeli bir paragraf varsa,
// yüksek seviyeli paragrafı daraltmak, düşük seviyeli paragrafı da daraltacaktır.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Aynı seviyedeki iki paragraf birbirini daraltmaz,
// ve oklar, işaret ettikleri paragrafları çökertmez.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// Varsayılan "BodyText" değeri en düşük seviyededir; herhangi bir seviyedeki paragraf bunu çökertebilir.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## Ayrıca Bakınız

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
