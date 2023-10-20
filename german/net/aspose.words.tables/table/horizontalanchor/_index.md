---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words für .NET
description: Table HorizontalAnchor eigendom. Ruft das Basisobjekt ab aus dem die horizontale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert istColumn  in C#.
type: docs
weight: 170
url: /de/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Ruft das Basisobjekt ab, aus dem die horizontale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert istColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

## Beispiele

Zeigt, wie mit Floating-Table-Eigenschaften gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Nur Rand, Seite, Spalte in RelativeHorizontalPosition für HorizontalAnchor-Setter verfügbar.
    // Die ArgumentException wird für alle anderen Werte ausgelöst.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Nur Rand, Seite, Absatz verfügbar in RelativeVerticalPosition für VerticalAnchor-Setter.
    // Die ArgumentException wird für alle anderen Werte ausgelöst.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Siehe auch

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
