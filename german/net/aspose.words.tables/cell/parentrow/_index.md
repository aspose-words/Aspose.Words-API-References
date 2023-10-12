---
title: Cell.ParentRow
second_title: Aspose.Words für .NET-API-Referenz
description: Cell eigendom. Gibt die übergeordnete Zeile der Zelle zurück.
type: docs
weight: 100
url: /de/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Gibt die übergeordnete Zeile der Zelle zurück.

```csharp
public Row ParentRow { get; }
```

### Bemerkungen

GleichwertigFirstNonMarkupParentNode gegossen zu[`Row`](../../row/).

### Beispiele

Zeigt, wie man eine Tabelle so einrichtet, dass sie auf derselben Seite bleibt.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// KeepWithNext für jeden Absatz in der Tabelle außer dem aktivieren
// Die letzten in der letzten Zeile verhindern, dass die Tabelle auf mehrere Seiten aufgeteilt wird.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Siehe auch

* class [Row](../../row/)
* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../cell/)
* Montage [Aspose.Words](../../../)


