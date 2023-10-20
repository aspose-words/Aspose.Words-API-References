---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words per .NET
description: Cell NextCell proprietà. Ottiene il successivoCell nodo in C#.
type: docs
weight: 70
url: /it/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Ottiene il successivo[`Cell`](../) nodo.

```csharp
public Cell NextCell { get; }
```

## Osservazioni

Il metodo può essere utilizzato quando è necessario avere accesso digitato alle celle di a[`Row`](../../row/) . Se a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) un nodo viene trovato in una riga invece che in una cella, viene automaticamente attraversato per ottenere una cella contenuta all'interno.

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

* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
