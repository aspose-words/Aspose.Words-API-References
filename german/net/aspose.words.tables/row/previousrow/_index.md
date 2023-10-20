---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words für .NET
description: Row PreviousRow eigendom. Ruft den vorherigen abRow node in C#.
type: docs
weight: 100
url: /de/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Ruft den vorherigen ab[`Row`](../) node.

```csharp
public Row PreviousRow { get; }
```

## Bemerkungen

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Tabellenzeilen benötigen. Wenn a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)Der Knoten wird in einer Tabelle statt in einer Zeile gefunden. Er wird automatisch durchlaufen, um eine darin enthaltene Zeile zu erhalten.

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

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
