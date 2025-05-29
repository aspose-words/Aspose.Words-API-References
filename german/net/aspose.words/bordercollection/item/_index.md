---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Entdecken Sie die BorderCollection-Elementeigenschaft, um einfach auf Border-Objekte nach Typ zuzugreifen. Optimieren Sie Ihr Design mit effizienter Rahmenverwaltung!
type: docs
weight: 60
url: /de/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

Ruft eine[`Border`](../../border/) Objekt nach Rahmentyp.

```csharp
public Border this[BorderType borderType] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| borderType | A[`BorderType`](../../bordertype/) value , der den Typ der abzurufenden Grenze angibt. |

## Bemerkungen

Beachten Sie, dass nicht alle Rahmen für verschiedene Dokumentelemente vorhanden sind. Diese Methode löst eine Ausnahme aus, wenn Sie einen Rahmen anfordern, der für das aktuelle Objekt nicht anwendbar ist.

## Beispiele

Zeigt, wie Sie Text mit Rahmen und Schattierungen verzieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### Siehe auch

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

Ruft eine[`Border`](../../border/) Objekt nach Index.

```csharp
public Border this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Nullbasierter Index der abzurufenden Grenze. |

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

* class [Border](../../border/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
