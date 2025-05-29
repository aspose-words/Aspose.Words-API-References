---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words per .NET
description: Scopri la proprietà NextRow per accedere senza problemi al nodo Riga successivo, migliorando l'esperienza di navigazione e gestione dei dati.
type: docs
weight: 70
url: /it/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Ottiene il prossimo[`Row`](../) nodo.

```csharp
public Row NextRow { get; }
```

## Osservazioni

Il metodo può essere utilizzato quando è necessario disporre di accesso tipizzato alle righe della tabella. Se a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) il nodo si trova in una tabella invece che in una riga, viene automaticamente attraversato per ottenere una riga in esso contenuta.

## Esempi

Mostra come enumerare tutte le celle della tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Enumera tutte le celle della tabella.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Guarda anche

* class [Row](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
