---
title: ParagraphFormat.KeepWithNext
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. True wenn der Absatz auf derselben Seite bleiben soll wie der darauf folgende Absatz.
type: docs
weight: 170
url: /de/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

True, wenn der Absatz auf derselben Seite bleiben soll wie der darauf folgende Absatz.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


