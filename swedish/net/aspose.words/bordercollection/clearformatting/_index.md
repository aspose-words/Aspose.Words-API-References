---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words för .NET
description: BorderCollection ClearFormatting metod. Tar bort alla kanter för ett objekt i C#.
type: docs
weight: 140
url: /sv/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Tar bort alla kanter för ett objekt.

```csharp
public void ClearFormatting()
```

## Exempel

Visar hur man tar bort alla ramar från alla stycken i ett dokument.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Det första stycket i detta dokument har synliga kanter med dessa inställningar.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Använd metoden "ClearFormatting" på varje stycke för att ta bort alla kanter.
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

### Se även

* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
