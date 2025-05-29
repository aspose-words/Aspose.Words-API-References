---
title: BorderCollection.Equals
linktitle: Equals
articleTitle: Equals
second_title: .NET için Aspose.Words
description: BorderCollection Equals yöntemini keşfederek border koleksiyonlarını verimli bir şekilde karşılaştırın ve kodlama üretkenliğinizi artırın. Projelerinizi bugün optimize edin!
type: docs
weight: 150
url: /tr/net/aspose.words/bordercollection/equals/
---
## BorderCollection.Equals method

Sınır koleksiyonlarını karşılaştırır.

```csharp
public bool Equals(BorderCollection brColl)
```

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

* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
