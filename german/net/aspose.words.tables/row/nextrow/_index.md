---
title: Row.NextRow
second_title: Aspose.Words für .NET-API-Referenz
description: Row eigendom. Ruft den nächsten abRow node.
type: docs
weight: 70
url: /de/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Ruft den nächsten ab[`Row`](../) node.

```csharp
public Row NextRow { get; }
```

### Bemerkungen

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Tabellenzeilen benötigen. Wenn a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)Der Knoten wird in einer Tabelle statt in einer Zeile gefunden. Er wird automatisch durchlaufen, um eine darin enthaltene Zeile zu erhalten.

### Beispiele

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
* namensraum [Aspose.Words.Tables](../../row/)
* Montage [Aspose.Words](../../../)


