---
title: Border.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Border GetHashCode-Methode, eine leistungsstarke Hash-Funktion, die die Datenintegrität und Leistung Ihrer Anwendungen verbessert. Schöpfen Sie noch heute ihr Potenzial!
type: docs
weight: 110
url: /de/net/aspose.words/border/gethashcode/
---
## Border.GetHashCode method

Dient als Hash-Funktion für diesen Typ.

```csharp
public override int GetHashCode()
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

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
