---
title: Paragraph.IsEndOfCell
second_title: Aspose.Words für .NET-API-Referenz
description: Paragraph eigendom. True wenn dieser Absatz der letzte Absatz in a istCell  sonst falsch.
type: docs
weight: 50
url: /de/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

True, wenn dieser Absatz der letzte Absatz in a ist[`Cell`](../../../aspose.words.tables/cell/) ; sonst falsch.

```csharp
public bool IsEndOfCell { get; }
```

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

* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)


