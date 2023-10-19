---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: Aspose.Words.Shading sınıf. Bir nesnenin gölgelendirme niteliklerini içerir C#'da.
type: docs
weight: 5990
url: /tr/net/aspose.words/shading/
---
## Shading class

Bir nesnenin gölgelendirme niteliklerini içerir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public class Shading : InternableComplexAttr
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Arka plana uygulanan rengi alır veya ayarlar.`Shading` nesne. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Bununla ilişkili uygulanan renk şemasındaki arka plan deseni tema rengini alır veya ayarlar.`Shading` nesne. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Arka plan tema rengini açan veya koyulaştıran çift değeri alır veya ayarlar. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Ön plana uygulanan rengi alır veya ayarlar.`Shading` nesne. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Bununla ilişkili uygulanan renk şemasında ön plan deseni tema rengini alır veya ayarlar.`Shading` nesne. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Ön plan tema rengini açan veya koyulaştıran bir çift değer alır veya ayarlar. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Gölgelendirme dokusunu alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Nesnedeki gölgelemeyi kaldırır. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Belirtilenin olup olmadığını belirler`Shading` şimdiki değere eşittir`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Bu tür için karma işlevi görevi görür. |

## Örnekler

Metnin kenarlıklar ve gölgelendirmeyle nasıl süsleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

Tablo oluştururken kenarlık ve gölgeleme renginin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir tablo başlatın ve kenarlıkları için varsayılan rengi/kalınlığı ayarlayın.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Farklı arka plan renklerine sahip iki hücreden oluşan bir satır oluşturun.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırlayın
// oluşturucu tarafından oluşturulan tüm yeni hücreler için özel bir kenar kalınlığı ayarlayın,
// sonra ikinci satırı oluşturalım.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Ayrıca bakınız

* class [InternableComplexAttr](../internablecomplexattr/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
