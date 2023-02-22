---
title: Border.IsVisible
second_title: Aspose.Words för .NET API Referens
description: Border fast egendom. Returnerar sant om LineStyle inte är LineStyle.None.
type: docs
weight: 30
url: /sv/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Returnerar sant om LineStyle inte är LineStyle.None.

```csharp
public bool IsVisible { get; }
```

### Exempel

Visar hur man tar bort kanter från ett stycke.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Varje stycke har en individuell uppsättning ramar.
// Vi kan komma åt inställningarna för utseendet på dessa gränser via objektet styckeformat.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

// Vi kan ta bort en kantlinje på en gång genom att köra metoden ClearFormatting. 
// Att köra den här metoden på varje kant i ett stycke tar bort alla dess kanter.
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
* namnutrymme [Aspose.Words](../../border/)
* hopsättning [Aspose.Words](../../../)


