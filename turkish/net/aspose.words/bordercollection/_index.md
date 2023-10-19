---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.BorderCollection sınıf. Bir koleksiyonBorder nesneler C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/bordercollection/
---
## BorderCollection class

Bir koleksiyon[`Border`](../border/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Alt kenarlığı alır. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Kenarlık rengini alır veya ayarlar. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Koleksiyondaki kenarlık sayısını alır. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Kenarlığın metinden uzaklığını nokta cinsinden alır veya ayarlar. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarlığı alır. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Bir öğeyi alır[`Border`](../border/) kenarlık türüne göre nesne. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Sol kenarlığı alır. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Kenarlık stilini alır veya ayarlar. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Kenarlık genişliğini nokta cinsinden alır veya ayarlar. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Doğru kenarlığı alır. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Üst kenarlığı alır. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Hücreler arasında kullanılan dikey kenarlığı alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Bir nesnenin tüm kenarlıklarını kaldırır. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Kenarlık koleksiyonlarını karşılaştırır. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Koleksiyondaki tüm kenarlıklar üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |

## Notlar

Farklı belge öğelerinin farklı sınırları vardır. Örneğin,[`ParagraphFormat`](../paragraphformat/)sahip olmak[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) Ve[`Top`](./top/) sınırlar. Her kenarlık için bağımsız olarak farklı biçimlendirme belirtebilirsiniz veya tüm kenarlıkları numaralandırıp aynı biçimlendirmeyi uygulayabilirsiniz.

## Örnekler

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

* class [Border](../border/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
