---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words for .NET
description: Aspose.Words.Border sınıf. Bir nesnenin kenarlığını temsil eder C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words/border/
---
## Border class

Bir nesnenin kenarlığını temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public class Border : InternableComplexAttr
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Kenarlık rengini alır veya ayarlar. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Kenarlığın metinden veya sayfa kenarından nokta cinsinden mesafesini alır veya ayarlar. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | İadeler`doğru` Eğer[`LineStyle`](./linestyle/) değilNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Kenarlık stilini alır veya ayarlar. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Kenarlık genişliğini nokta cinsinden alır veya ayarlar. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Bu Border nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır veya ayarlar. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Bir rengi açan veya koyulaştıran double değerini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Kenarlık özelliklerini varsayılan değerlere sıfırlar. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | Belirtilen kenarlığın değer olarak geçerli kenarlığa eşit olup olmadığını belirler. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Bu tür için karma işlevi görevi görür. |

## Notlar

Kenarlıklar, paragraf, paragraf veya tablo hücresi içindeki metin dizisi dahil olmak üzere çeşitli belge öğelerine uygulanabilir.

## Örnekler

Kenarlıkla çevrelenmiş bir dizenin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Üst kenarlığı olan bir paragrafın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor'ı yalnızca LineWidth veya LineStyle ayarlandığında ayarlayın.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ayrıca bakınız

* class [InternableComplexAttr](../internablecomplexattr/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
