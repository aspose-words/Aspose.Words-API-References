---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words per .NET
description: Accedi alla proprietà PreviousRow per recuperare facilmente il nodo Row precedente, migliorando la navigazione dei dati e semplificando il flusso di lavoro di codifica.
type: docs
weight: 100
url: /it/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Ottiene il precedente[`Row`](../) nodo.

```csharp
public Row PreviousRow { get; }
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
