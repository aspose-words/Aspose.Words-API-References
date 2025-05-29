---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words per .NET
description: Rimuovi facilmente righe dalle tabelle con il metodo DeleteRow di DocumentBuilder. Semplifica la modifica dei documenti e migliora il flusso di lavoro!
type: docs
weight: 200
url: /it/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Elimina una riga da una tabella.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableIndex | Int32 | L'indice della tabella. |
| rowIndex | Int32 | L'indice della riga nella tabella. |

### Valore di ritorno

Il nodo della riga che è stato appena rimosso.

## Osservazioni

Se il cursore si trova all'interno della riga che viene eliminata, il cursore viene spostato alla riga successiva o al paragrafo successivo dopo la tabella.

Se si elimina una riga da una tabella che contiene una sola riga, verrà eliminata l'intera tabella x000d_.

Per i parametri indice, quando indice è maggiore o uguale a 0, specifica un indice da all'inizio, con 0 come primo elemento. Quando indice è minore di 0, specifica un indice da alla fine, con -1 come ultimo elemento.

## Esempi

Mostra come eliminare una riga da una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Elimina la prima riga della prima tabella nel documento.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Guarda anche

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
