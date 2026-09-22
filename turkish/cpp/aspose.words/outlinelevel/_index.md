---
title: "Aspose::Words::OutlineLevel enum"
linktitle: "OutlineLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::OutlineLevel enum. C++'da belgedeki bir paragrafın anahat seviyesini belirtir."
type: docs
weight: 105000
url: /tr/cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


Belgedeki bir paragrafın taslak seviyesini belirtir.

```cpp
enum class OutlineLevel
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Level1 | 0 | Paragraf, anahat seviyesi 1'de (en üst seviye) bulunur. |
| Level2 | 1 | Paragraf, taslak seviyesi 2'de bulunur. |
| Level3 | 2 | Paragraf, taslak seviyesi 3'de bulunur. |
| Level4 | 3 | Paragraf, taslak seviyesi 4'de bulunur. |
| Level5 | 4 | Paragraf, taslak seviyesi 5'de bulunur. |
| Level6 | 5 | Paragraf, taslak seviyesi 6'de bulunur. |
| Level7 | 6 | Paragraf, taslak seviyesi 7'de bulunur. |
| Level8 | 7 | Paragraf, taslak seviyesi 8'de bulunur. |
| Level9 | 8 | Paragraf, taslak seviyesi 9'de bulunur. |
| BodyText | 9 | Paragraf, ana metin seviyesinde bulunur. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
