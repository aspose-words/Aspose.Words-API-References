---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: BorderCollection Item mülk. Bir öğeyi alırBorder kenarlık türüne göre nesne C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

Bir öğeyi alır[`Border`](../../border/) kenarlık türüne göre nesne.

```csharp
public Border this[BorderType borderType] { get; }
```

| Parametre | Tanım |
| --- | --- |
| borderType | A[`BorderType`](../../bordertype/) Alınacak kenarlığın türünü belirten değer . |

## Notlar

Farklı belge öğeleri için tüm kenarlıkların mevcut olmadığını unutmayın. Geçerli nesneye uygulanamayan bir kenarlık talep ederseniz bu yöntem bir istisna atar.

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

### Ayrıca bakınız

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

Bir öğeyi alır[`Border`](../../border/) indekse göre nesne.

```csharp
public Border this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Alınacak sınırın sıfır tabanlı dizini. |

## Örnekler

Kenarlık koleksiyonlarının öğeleri nasıl paylaşabildiğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Oluştururken aynı border konfigürasyonunu kullandığımız için
// bu paragraflar, kenar koleksiyonları aynı unsurları paylaşıyor.
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

// Sadece ikinci paragrafta kenarlıkların çizgi stilini değiştirdikten sonra,
// kenarlık koleksiyonları artık aynı öğeleri paylaşmıyor.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Boş bir kenarlığın görünümünü değiştirmek onu görünür kılar.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Ayrıca bakınız

* class [Border](../../border/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
