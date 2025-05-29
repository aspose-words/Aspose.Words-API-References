---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Zellenabsätze“, um auf eine Sammlung direkt untergeordneter Absätze zuzugreifen und so die Struktur und Lesbarkeit Ihres Dokuments zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Zelle sind.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
