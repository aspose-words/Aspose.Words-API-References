---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi için Border nesnelerini zahmetsizce yönetmek ve özelleştirmek için başvuracağınız çözüm olan Aspose.Words.BorderCollection'ı keşfedin.
type: docs
weight: 280
url: /tr/net/aspose.words/bordercollection/
---
## BorderCollection class

Bir koleksiyon[`Border`](../border/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Alt sınırı alır. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Sınır rengini alır veya ayarlar. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Koleksiyondaki kenarlık sayısını alır. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Sınırın metinden uzaklığını noktalar halinde alır veya ayarlar. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarlığı alır. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Birini alır[`Border`](../border/) sınır türüne göre nesne. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Sol kenarlığı alır. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Kenarlık stilini alır veya ayarlar. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Sınır genişliğini noktalar halinde alır veya ayarlar. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Doğru sınırı alır. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Sınırın gölgesi olup olmadığını belirten bir değer alır veya ayarlar. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Üst sınırı alır. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Hücreler arasında kullanılan dikey kenarlığı alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Bir nesnenin tüm kenarlıklarını kaldırır. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Sınır koleksiyonlarını karşılaştırır. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Koleksiyondaki tüm sınırlar üzerinde yineleme yapmak için kullanılabilecek bir numaratör nesnesi döndürür. |

## Notlar

Farklı belge öğelerinin farklı sınırları vardır. Örneğin,[`ParagraphFormat`](../paragraphformat/) sahip olmak[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) Ve[`Top`](./top/) borders. Her bir kenarlık için bağımsız olarak farklı biçimlendirme belirleyebilir veya tüm kenarlıkları numaralandırıp aynı biçimlendirmeyi uygulayabilirsiniz.

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
