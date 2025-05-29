---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Row IsLastRow“. Identifizieren Sie mühelos, ob eine Zeile die letzte in einer Tabelle ist, und optimieren Sie so die Datenverwaltung und die Programmiereffizienz.
type: docs
weight: 50
url: /de/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Wahr, wenn dies die letzte Zeile in einer Tabelle ist, andernfalls falsch.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
