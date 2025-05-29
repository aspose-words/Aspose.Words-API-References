---
title: BorderCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BorderCollection Count för att enkelt komma åt det totala antalet ramar, vilket förbättrar din designflexibilitet och effektivitet.
type: docs
weight: 30
url: /sv/net/aspose.words/bordercollection/count/
---
## BorderCollection.Count property

Hämtar antalet ramar i samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar hur kantsamlingar kan dela element.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Eftersom vi använde samma kantkonfiguration när vi skapade
// dessa stycken, deras kantsamlingar delar samma element.
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

// Efter att ha ändrat linjestilen för kantlinjerna i bara det andra stycket,
// kantsamlingarna delar inte längre samma element.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Att ändra utseendet på en tom ram gör den synlig.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Se även

* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
