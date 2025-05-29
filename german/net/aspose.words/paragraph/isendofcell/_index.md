---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsEndOfCell-Eigenschaft für Absätze. Erfahren Sie, wie Sie erkennen, ob ein Absatz der letzte in einer Zelle ist, und so Ihre Dokumentstruktur verbessern.
type: docs
weight: 50
url: /de/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Wahr, wenn dieser Absatz der letzte Absatz in einem[`Cell`](../../../aspose.words.tables/cell/) ; andernfalls false.

```csharp
public bool IsEndOfCell { get; }
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

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
