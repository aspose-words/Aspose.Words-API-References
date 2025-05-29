---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: .NET için Aspose.Words
description: BorderCollection ClearFormatting yönteminin tüm nesne kenarlıklarını zahmetsizce nasıl kaldırdığını ve tasarımınızı temiz, keskin görsellerle nasıl geliştirdiğini keşfedin.
type: docs
weight: 140
url: /tr/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Bir nesnenin tüm kenarlıklarını kaldırır.

```csharp
public void ClearFormatting()
```

## Örnekler

Bir belgedeki tüm paragraflardaki tüm kenarlıkların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Bu belgenin ilk paragrafında bu ayarlarla görünür kenarlıklar vardır.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Her paragrafta tüm kenarlıkları kaldırmak için "ClearFormatting" yöntemini kullanın.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### Ayrıca bakınız

* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
