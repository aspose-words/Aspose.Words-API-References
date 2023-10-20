---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words für .NET
description: Cell PreviousCell eigendom. Ruft den vorherigen abCell node in C#.
type: docs
weight: 110
url: /de/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

Ruft den vorherigen ab[`Cell`](../) node.

```csharp
public Cell PreviousCell { get; }
```

## Bemerkungen

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Zellen von a benötigen[`Row`](../../row/) . Wenn a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Wird ein Knoten in einer Zeile statt in einer Zelle gefunden, wird er automatisch durchlaufen, um eine darin enthaltene Zelle zu erhalten.

## Beispiele

Zeigt, wie alle Tabellenzellen aufgezählt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Alle Zellen der Tabelle aufzählen.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Siehe auch

* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
