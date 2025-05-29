---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: .NET için Aspose.Words
description: Özelleştirilebilir paragraf satır aralığı için Aspose.Words.LineSpacingRule enum'unu keşfedin. Hassas kontrol ve iyileştirilmiş okunabilirlikle belge biçimlendirmesini geliştirin.
type: docs
weight: 3890
url: /tr/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Bir paragraf için satır aralığı değerlerini belirtir.

```csharp
public enum LineSpacingRule
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| AtLeast | `0` | Satır aralığı, belirtilen değerden büyük veya eşit olabilir, ancak asla değerinden küçük olamaz.[`LineSpacing`](../paragraphformat/linespacing/) mülk. |
| Exactly | `1` | Satır aralığı, içinde belirtilen değerden asla değişmez.[`LineSpacing`](../paragraphformat/linespacing/) özellik, paragrafta daha büyük bir yazı tipi kullanılsa bile. |
| Multiple | `2` | Satır aralığı şu şekilde belirtilir:[`LineSpacing`](../paragraphformat/linespacing/) özelliği satır sayısı olarak. Bir satır 12 noktaya eşittir. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
