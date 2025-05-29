---
title: Border.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: .NET için Aspose.Words
description: Uygulamalarınız için veri bütünlüğünü ve performansı artıran güçlü bir karma işlevi olan Border GetHashCode yöntemini keşfedin. Potansiyelini bugün açığa çıkarın!
type: docs
weight: 110
url: /tr/net/aspose.words/border/gethashcode/
---
## Border.GetHashCode method

Bu tür için bir karma işlevi görevi görür.

```csharp
public override int GetHashCode()
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

* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
