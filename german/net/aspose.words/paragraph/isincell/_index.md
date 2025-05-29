---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsInCell-Eigenschaft des Absatzes. Ermitteln Sie ganz einfach, ob ein Absatz ein direktes untergeordnetes Element einer Zelle ist, und verbessern Sie so die Struktur und Formatierung Ihres Dokuments.
type: docs
weight: 100
url: /de/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Wahr, wenn dieser Absatz ein unmittelbares Kind von[`Cell`](../../../aspose.words.tables/cell/) ; andernfalls false.

```csharp
public bool IsInCell { get; }
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
