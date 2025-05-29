---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words für .NET
description: Entdecken Sie die NextCell-Eigenschaft, um einfach auf den nächsten Zellknoten zuzugreifen, Ihr Datenmanagement zu verbessern und Ihren Arbeitsablauf zu optimieren.
type: docs
weight: 70
url: /de/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Ruft den nächsten[`Cell`](../) Knoten.

```csharp
public Cell NextCell { get; }
```

## Bemerkungen

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Zellen einer[`Row`](../../row/) Wenn a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Wenn ein Knoten in einer Zeile statt in einer Zelle gefunden wird, wird er automatisch durchlaufen, um eine darin enthaltene Zelle zu finden.

## Beispiele

Zeigt, wie alle Tabellenzellen durchnummeriert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Alle Zellen der Tabelle durchzählen.
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
