---
title: Table.FirstRow
linktitle: FirstRow
articleTitle: FirstRow
second_title: Aspose.Words per .NET
description: Scopri la proprietà FirstRow delle tabelle, accedi senza sforzo al nodo della prima riga per una gestione semplificata dei dati e funzionalità avanzate delle tabelle.
type: docs
weight: 160
url: /it/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

Restituisce il primo[`Row`](../../row/) nodo nella tabella.

```csharp
public Row FirstRow { get; }
```

## Esempi

Mostra come rimuovere la prima e l'ultima riga di tutte le tabelle in un documento.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tabelle" di un nodo Corpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzo del metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe dalla tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Guarda anche

* class [Row](../../row/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
