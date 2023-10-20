---
title: Border.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words für .NET
description: Border Equals methode. Bestimmt ob der angegebene Rahmen den gleichen Wert wie der aktuelle Rahmen hat in C#.
type: docs
weight: 100
url: /de/net/aspose.words/border/equals/
---
## Equals(*[Border](../)*) {#equals}

Bestimmt, ob der angegebene Rahmen den gleichen Wert wie der aktuelle Rahmen hat.

```csharp
public bool Equals(Border rhs)
```

## Beispiele

Zeigt, wie Rahmensammlungen Elemente gemeinsam nutzen können.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Da wir beim Erstellen dieselbe Rahmenkonfiguration verwendet haben
// Diese Absätze und ihre Randsammlungen haben dieselben Elemente.
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

// Nachdem der Linienstil der Ränder nur im zweiten Absatz geändert wurde,
// Die Border-Sammlungen teilen nicht mehr dieselben Elemente.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Durch Ändern des Erscheinungsbilds eines leeren Rahmens wird dieser sichtbar.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Siehe auch

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat.

```csharp
public override bool Equals(object obj)
```

## Beispiele

Zeigt, wie Rahmensammlungen Elemente gemeinsam nutzen können.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Da wir beim Erstellen dieselbe Rahmenkonfiguration verwendet haben
// Diese Absätze und ihre Randsammlungen haben dieselben Elemente.
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

// Nachdem der Linienstil der Ränder nur im zweiten Absatz geändert wurde,
// Die Border-Sammlungen teilen nicht mehr dieselben Elemente.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Durch Ändern des Erscheinungsbilds eines leeren Rahmens wird dieser sichtbar.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Siehe auch

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
