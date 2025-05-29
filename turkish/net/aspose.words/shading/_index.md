---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: .NET için Aspose.Words
description: Profesyonel bir görünüm için özelleştirilebilir gölgelendirme nitelikleriyle belgelerinizi geliştirmek üzere tasarlanmış Aspose.Words.Shading sınıfını keşfedin.
type: docs
weight: 6820
url: /tr/net/aspose.words/shading/
---
## Shading class

Bir nesne için gölgelendirme niteliklerini içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class Shading : InternableComplexAttr
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Arka plana uygulanan rengi alır veya ayarlar`Shading` nesne. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Bu renk şemasıyla ilişkili uygulanan renk şemasındaki arka plan desen teması rengini alır veya ayarlar`Shading` nesne. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Arka plan tema rengini açan veya koyulaştıran bir çift değer alır veya ayarlar. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Ön plana uygulanan rengi alır veya ayarlar`Shading` nesne. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Bu renk şemasıyla ilişkili uygulanan renk şemasındaki ön plan desen teması rengini alır veya ayarlar`Shading` nesne. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Ön plandaki temanın rengini açan veya koyulaştıran bir çift değer alır veya ayarlar. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Gölgelendirme dokusunu alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Nesneden gölgelendirmeyi kaldırır. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Belirtilenin geçerli olup olmadığını belirler`Shading` mevcut değere eşittir`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Bu tür için bir karma işlevi görevi görür. |

## Örnekler

Metnin kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

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

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir tablo başlatın ve kenarlıkları için varsayılan bir renk/kalınlık ayarlayın.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Farklı arka plan renklerine sahip iki hücreden oluşan bir satır oluştur.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırlayın
// Oluşturucu tarafından oluşturulan tüm yeni hücreler için özel bir kenarlık kalınlığı ayarlayın,
// daha sonra ikinci bir satır oluştur.
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
