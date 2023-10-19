---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words for .NET
description: ParagraphFormat LineSpacing mülk. Paragrafın satır aralığını nokta cinsinden alır veya ayarlar C#'da.
type: docs
weight: 190
url: /tr/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Paragrafın satır aralığını (nokta cinsinden) alır veya ayarlar.

```csharp
public double LineSpacing { get; set; }
```

## Notlar

Ne zaman[`LineSpacingRule`](../linespacingrule/) özellik şu şekilde ayarlandı:AtLeast satır aralığı, 'den büyük veya ona eşit olabilir ancak asla belirtilenden az olamaz`LineSpacing` değer.

Ne zaman[`LineSpacingRule`](../linespacingrule/) özellik şu şekilde ayarlandı:Exactly , satır aralığı hiçbir zaman belirtilen from değişmez`LineSpacing` Paragrafta daha büyük bir yazı tipi kullanılsa bile değer.

## Örnekler

Satır aralığıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, aşağıdakileri kullanarak tanımlayabileceğimiz üç satır aralığı kuralı verilmiştir:
// paragraflar arasındaki boşluğu yapılandırmak için paragrafın "LineSpacingRule" özelliği.
// 1 - Minimum boşluk miktarını ayarlayın.
// Bu, her boyuttaki metin satırlarına dikey dolgu sağlar
// bu minimum satır yüksekliğini korumak için çok küçük.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Tam aralığı ayarlayın.
// Boşluk için çok büyük yazı tipi boyutlarının kullanılması metnin kesilmesine neden olur.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Aralığı, varsayılan olarak 12 punto olan varsayılan satır aralığının katı olarak ayarlayın.
// Bu tür boşluklar farklı yazı tipi boyutlarına göre ölçeklenecektir.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
