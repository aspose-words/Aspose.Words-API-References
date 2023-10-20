---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words für .NET
description: Cell NextCell eigendom. Ruft den nächsten abCell node in C#.
type: docs
weight: 70
url: /de/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Ruft den nächsten ab[`Cell`](../) node.

```csharp
public Cell NextCell { get; }
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
