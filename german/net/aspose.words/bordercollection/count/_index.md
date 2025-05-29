---
title: BorderCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die BorderCollection Count-Eigenschaft, um einfach auf die Gesamtzahl der Rahmen zuzugreifen und so Ihre Designflexibilität und -effizienz zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words/bordercollection/count/
---
## BorderCollection.Count property

Ruft die Anzahl der Ränder in der Sammlung ab.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie Rahmensammlungen Elemente gemeinsam nutzen können.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Da wir beim Erstellen die gleiche Rahmenkonfiguration verwendet haben
// Diese Absätze und ihre Randsammlungen weisen dieselben Elemente auf.
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

// Nachdem ich den Linienstil der Rahmen nur im zweiten Absatz geändert habe,
// Die Randsammlungen weisen nicht mehr dieselben Elemente auf.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
