---
title: Class BorderCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.BorderCollection sınıf. Border nesneleri koleksiyonu.
type: docs
weight: 80
url: /tr/net/aspose.words/bordercollection/
---
## BorderCollection class

Border nesneleri koleksiyonu.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Alt kenarlığı alır. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Kenarlık rengini alır veya ayarlar. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Koleksiyondaki kenarlık sayısını alır. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Kenarlığın metne olan mesafesini noktalar olarak alır veya ayarlar. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarlığı alır. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Kenarlık türüne göre bir Border nesnesi alır. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Sol kenarlığı alır. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Kenarlık stilini alır veya ayarlar. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Kenarlık genişliğini nokta olarak alır veya ayarlar. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Sağ kenarlığı alır. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Üst sınırı alır. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Hücreler arasında kullanılan dikey kenarlığı alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Bir nesnenin tüm kenarlıklarını kaldırır. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(BorderCollection) | Kenarlık koleksiyonlarını karşılaştırır. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Koleksiyondaki tüm kenarlıklar üzerinde yineleme yapmak için kullanılabilecek bir Numaralandırıcı nesnesi döndürür. |

### Notlar

Farklı belge öğelerinin farklı kenarlıkları vardır. Örneğin, ParagraphFormat'ın Alt, Sol, Sağ ve Üst kenarlıkları vardır. Her kenarlık için bağımsız olarak farklı biçimlendirme belirleyebilir veya tüm kenarlıklar arasında numaralandırabilir ve aynı biçimlendirmeyi uygulayabilirsiniz.

### Örnekler

Üst kenarlıklı bir paragrafın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ayrıca bakınız

* class [Border](../border/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


