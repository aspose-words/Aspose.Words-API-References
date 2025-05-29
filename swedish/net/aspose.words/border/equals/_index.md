---
title: Border.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words för .NET
description: Upptäck metoden Border Equals för att enkelt jämföra kantvärden och förbättra din designprecision. Uppnå konsekventa resultat utan problem!
type: docs
weight: 100
url: /sv/net/aspose.words/border/equals/
---
## Equals(*[Border](../)*) {#equals}

Avgör om den angivna ramen har samma värde som den aktuella ramen.

```csharp
public bool Equals(Border rhs)
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

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Avgör om det angivna objektet har samma värde som det aktuella objektet.

```csharp
public override bool Equals(object obj)
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

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
