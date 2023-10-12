---
title: Cell.Paragraphs
second_title: Aspose.Words für .NET-API-Referenz
description: Cell eigendom. Ruft eine Sammlung von Absätzen ab die unmittelbar untergeordnete Elemente der Zelle sind.
type: docs
weight: 90
url: /de/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Ruft eine Sammlung von Absätzen ab, die unmittelbar untergeordnete Elemente der Zelle sind.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../cell/)
* Montage [Aspose.Words](../../../)


