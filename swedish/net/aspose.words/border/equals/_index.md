---
title: Border.Equals
second_title: Aspose.Words för .NET API Referens
description: Border metod. Bestämmer om den angivna gränsen är lika i värde med den aktuella gränsen.
type: docs
weight: 100
url: /sv/net/aspose.words/border/equals/
---
## Equals(Border) {#equals}

Bestämmer om den angivna gränsen är lika i värde med den aktuella gränsen.

```csharp
public bool Equals(Border rhs)
```

### Exempel

Visar hur gränssamlingar kan dela element.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Eftersom vi använde samma kantkonfiguration när vi skapade
// dessa stycken, deras gränssamlingar delar samma element.
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

// Efter att ha ändrat linjestilen för kanterna i bara det andra stycket,
// gränssamlingarna delar inte längre samma element.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Att ändra utseendet på en tom kant gör den synlig.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../border/)
* hopsättning [Aspose.Words](../../../)

---

## Equals(object) {#equals_1}

Bestämmer om det angivna objektet har samma värde som det aktuella objektet.

```csharp
public override bool Equals(object obj)
```

### Exempel

Visar hur gränssamlingar kan dela element.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Eftersom vi använde samma kantkonfiguration när vi skapade
// dessa stycken, deras gränssamlingar delar samma element.
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

// Efter att ha ändrat linjestilen för kanterna i bara det andra stycket,
// gränssamlingarna delar inte längre samma element.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Att ändra utseendet på en tom kant gör den synlig.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../border/)
* hopsättning [Aspose.Words](../../../)


