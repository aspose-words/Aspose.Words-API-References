---
title: BorderCollection.Count
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection eigendom. Ruft die Anzahl der Rahmen in der Sammlung ab.
type: docs
weight: 30
url: /de/net/aspose.words/bordercollection/count/
---
## BorderCollection.Count property

Ruft die Anzahl der Rahmen in der Sammlung ab.

```csharp
public int Count { get; }
```

### Beispiele

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

* class [BorderCollection](../)
* namensraum [Aspose.Words](../../bordercollection/)
* Montage [Aspose.Words](../../../)


