---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words für .NET
description: Entdecken Sie die Cell ParentRow-Eigenschaft, um einfach auf die übergeordnete Zeile einer beliebigen Zelle zuzugreifen und so die Effizienz Ihrer Datenverwaltung und Navigation zu verbessern.
type: docs
weight: 100
url: /de/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Gibt die übergeordnete Zeile der Zelle zurück.

```csharp
public Row ParentRow { get; }
```

## Beispiele

Zeigt, wie man einen Tisch einrichtet, damit alle Beteiligten auf dem gleichen Stand bleiben.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Aktivieren von KeepWithNext für jeden Absatz in der Tabelle außer dem
// Die letzten in der letzten Zeile verhindern, dass die Tabelle auf mehrere Seiten aufgeteilt wird.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
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
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
