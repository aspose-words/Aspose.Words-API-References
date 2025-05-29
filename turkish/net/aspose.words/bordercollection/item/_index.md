---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: BorderCollection Item özelliğini keşfedin ve Border nesnelerine türlerine göre kolayca erişin. Verimli border yönetimiyle tasarımınızı kolaylaştırın!
type: docs
weight: 60
url: /tr/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

Birini alır[`Border`](../../border/) sınır türüne göre nesne.

```csharp
public Border this[BorderType borderType] { get; }
```

| Parametre | Tanım |
| --- | --- |
| borderType | A[`BorderType`](../../bordertype/) Alınacak sınırın türünü belirten value . |

## Notlar

Tüm kenarlıkların farklı belge öğeleri için mevcut olmadığını unutmayın. Bu yöntem, geçerli nesneye uygulanamayan bir kenarlık isteğinde bulunursanız bir istisna fırlatır.

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

### Ayrıca bakınız

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

Birini alır[`Border`](../../border/) nesne index. tarafından

```csharp
public Border this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Alınacak sınırın sıfır tabanlı indeksi. |

## Örnekler

Sınır koleksiyonlarının öğeleri nasıl paylaşabileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Oluştururken aynı sınır yapılandırmasını kullandığımızdan
// Bu paragrafların kenarlık koleksiyonları aynı öğeleri paylaşır.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// Sadece ikinci paragraftaki sınırların çizgi stilini değiştirdikten sonra,
// sınır koleksiyonları artık aynı öğeleri paylaşmıyor.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Boş bir kenarlığın görünümünü değiştirmek onu görünür hale getirir.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Ayrıca bakınız

* class [Border](../../border/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
