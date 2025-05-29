---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words für .NET
description: Entdecken Sie die NextRow-Eigenschaft, um mühelos auf den folgenden Zeilenknoten zuzugreifen und so Ihre Datennavigation und -verwaltung zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Ruft den nächsten[`Row`](../) Knoten.

```csharp
public Row NextRow { get; }
```

## Bemerkungen

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Tabellenzeilen benötigen. Wenn a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Wenn ein Knoten in einer Tabelle statt in einer Zeile gefunden wird, wird er automatisch durchlaufen, um eine darin enthaltene Zeile zu erhalten.

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

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
