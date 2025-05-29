---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ParagraphFormat-Eigenschaft „KeepWithNext“ dafür sorgt, dass Ihre Absätze zusammenbleiben, wodurch der Dokumentfluss und die Lesbarkeit verbessert werden und ein elegantes Erscheinungsbild entsteht.
type: docs
weight: 170
url: /de/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Wahr, wenn der Absatz auf derselben Seite bleiben soll wie der darauf folgende Absatz.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
