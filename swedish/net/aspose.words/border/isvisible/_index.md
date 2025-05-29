---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen Border IsVisible förbättrar din design genom att returnera sant när LineStyle tillämpas. Optimera ditt användargränssnitt med den här viktiga funktionen!
type: docs
weight: 30
url: /sv/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Returer`sann` om den[`LineStyle`](../linestyle/) är inteNone .

```csharp
public bool IsVisible { get; }
```

## Exempel

Visar hur man tar bort ramar från ett stycke.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Varje stycke har en individuell uppsättning ramar.
// Vi kan komma åt inställningarna för utseendet på dessa ramar via styckeformatobjektet.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Vi kan ta bort en kantlinje direkt genom att köra ClearFormatting-metoden.
// Om du kör den här metoden på varje kantlinje i ett stycke tas alla dess kantlinjer bort.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
