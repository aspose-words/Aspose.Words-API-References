---
title: Border.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words för .NET
description: Återställ dina kantegenskaper till standardinställningarna med metoden Border ClearFormatting. Förenkla din designprocess och förbättra ditt projekts utseende!
type: docs
weight: 90
url: /sv/net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

Återställer kantegenskaperna till standardvärdena.

```csharp
public void ClearFormatting()
```

## Anmärkningar

När kantegenskaperna återställs till standardvärdena är kantlinjen osynlig.

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
