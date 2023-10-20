---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words für .NET
description: Row IsLastRow eigendom. True wenn dies die letzte Zeile in einer Tabelle ist sonst falsch in C#.
type: docs
weight: 50
url: /de/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

True, wenn dies die letzte Zeile in einer Tabelle ist; sonst falsch.

```csharp
public bool IsLastRow { get; }
```

## Beispiele

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

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
