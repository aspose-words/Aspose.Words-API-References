---
title: "Aspose::Words::LineSpacingRule enum"
linktitle: "LineSpacingRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LineSpacingRule enum. C++'de bir paragraf için satır aralığı değerlerini belirtir."
type: docs
weight: 95000
url: /tr/cpp/aspose.words/linespacingrule/
---
## LineSpacingRule enum


Bir paragraf için satır aralığı değerlerini belirtir.

```cpp
enum class LineSpacingRule
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| AtLeast | 0 | Satır aralığı, [LineSpacing](../paragraphformat/get_linespacing/) özelliğinde belirtilen değerden büyük veya eşit olabilir, ancak asla daha küçük olamaz. |
| Exactly | 1 | Satır aralığı, paragraf içinde daha büyük bir yazı tipi kullanılsa bile, [LineSpacing](../paragraphformat/get_linespacing/) özelliğinde belirtilen değerden asla değişmez. |
| Multiple | 2 | Satır aralığı, [LineSpacing](../paragraphformat/get_linespacing/) özelliğinde satır sayısı olarak belirtilir. Bir satır 12 puana eşittir. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
