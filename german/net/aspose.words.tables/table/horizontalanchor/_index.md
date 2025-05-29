---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Table HorizontalAnchor“, um die Positionierung schwebender Tabellen zu optimieren. Passen Sie die horizontale Ausrichtung einfach an und optimieren Sie so die Layoutkontrolle.
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

Zeigt, wie mit den Eigenschaften schwebender Tabellen gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Für den HorizontalAnchor-Setter sind in RelativeHorizontalPosition nur Margin, Page und Column verfügbar.
    // Für alle anderen Werte wird die ArgumentException ausgelöst.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Für den VerticalAnchor-Setter sind in RelativeVerticalPosition nur Margin, Page und Paragraph verfügbar.
    // Für alle anderen Werte wird die ArgumentException ausgelöst.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Siehe auch

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
