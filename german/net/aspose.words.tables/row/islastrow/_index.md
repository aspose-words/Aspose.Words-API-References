---
title: IsLastRow
second_title: Aspose.Words für .NET-API-Referenz
description: True wenn dies die letzte Zeile in einer Tabelle ist andernfalls falsch.
type: docs
weight: 50
url: /de/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

True, wenn dies die letzte Zeile in einer Tabelle ist; andernfalls falsch.

```csharp
public bool IsLastRow { get; }
```

### Beispiele

Zeigt, wie man einen Tisch so einrichtet, dass er zusammen auf der gleichen Seite bleibt.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Aktiviere KeepWithNext für jeden Absatz in der Tabelle außer dem
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

* class [Row](../../row)
* namensraum [Aspose.Words.Tables](../../row)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
