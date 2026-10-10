---
title: "Aspose::Words::ParagraphFormat::get_LineSpacing metodu"
linktitle: "get_LineSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_LineSpacing metodu. C++'ta paragraf için satır aralığını (nokta cinsinden) alır veya ayarlar."
type: docs
weight: 20000
url: /tr/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


Paragraf için satır aralığını (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## Açıklamalar


[LineSpacingRule](../get_linespacingrule/) özelliği [AtLeast](../../linespacingrule/) olarak ayarlandığında, satır aralığı belirtilen [LineSpacing](./) değerine eşit veya daha büyük olabilir, ancak asla daha düşük olamaz.

[LineSpacingRule](../get_linespacingrule/) özelliği [Exactly](../../linespacingrule/) olarak ayarlandığında, satır aralığı belirtilen [LineSpacing](./) değerinden asla değişmez, paragrafta daha büyük bir yazı tipi kullanılsa bile.

## Örnekler



Satır aralığıyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda, kullanarak tanımlayabileceğimiz üç satır aralığı kuralı bulunmaktadır
// paragrafın "LineSpacingRule" özelliği, paragraflar arasındaki aralığı yapılandırmak için.
// 1 -  Minimum bir boşluk miktarı ayarla.
// Bu, herhangi bir boyuttaki metin satırlarına dikey dolgu sağlar
// ki bu, minimum satır yüksekliğini korumak için çok küçüktür.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Kesin aralığı ayarla.
// Aralık için çok büyük punto boyutları kullanmak metni kırpacaktır.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Aralığı, varsayılan satır aralığının katı olarak ayarla, varsayılan olarak 12 puandır.
// Bu tür aralık farklı **font sizes**'a ölçeklenecektir.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
