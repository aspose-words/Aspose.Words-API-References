---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: .NET için Aspose.Words
description: ParagraphFormat LineSpacing özelliğiyle paragraflarınızın satır aralığını zahmetsizce ayarlayın. Belgelerinizdeki okunabilirliği ve stili geliştirin!
type: docs
weight: 190
url: /tr/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Paragraf için satır aralığını (nokta cinsinden) alır veya ayarlar.

```csharp
public double LineSpacing { get; set; }
```

## Notlar

Ne zaman[`LineSpacingRule`](../linespacingrule/) mülk ayarlandıAtLeast , satır aralığı, 'den büyük veya ona eşit olabilir ancak belirtilen değerden asla daha az olamaz`LineSpacing` değer.

Ne zaman[`LineSpacingRule`](../linespacingrule/) mülk ayarlandıExactly , satır aralığı belirtilen 'den asla değişmez`LineSpacing` Paragraf içerisinde daha büyük bir yazı tipi kullanılsa bile değer değişmez.

## Örnekler

Satır aralıklarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, kullanarak tanımlayabileceğimiz üç satır aralığı kuralı bulunmaktadır.
// Paragraflar arasındaki boşlukları yapılandırmak için paragrafın "LineSpacingRule" özelliği.
// 1 - Minimum aralık miktarını ayarlayın.
// Bu, herhangi bir boyuttaki metin satırlarına dikey dolgu verecektir
// minimum satır yüksekliğini korumak için çok küçük.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Tam aralığı ayarlayın.
// Boşluklara göre çok büyük yazı tipi boyutları kullanmak metni kesecektir.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Varsayılan satır aralığının (varsayılan olarak 12 punto) katı olarak aralık ayarlayın.
// Bu tür aralıklar farklı yazı tipi boyutlarına göre ölçeklenecektir.
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
