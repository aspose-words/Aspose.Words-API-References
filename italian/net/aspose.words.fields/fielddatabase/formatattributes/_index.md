---
title: FieldDatabase.FormatAttributes
linktitle: FormatAttributes
articleTitle: FormatAttributes
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldDatabase FormatAttributes per personalizzare facilmente gli attributi della tabella, migliorando la gestione e la presentazione dei dati.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fielddatabase/formatattributes/
---
## FieldDatabase.FormatAttributes property

Ottiene o imposta quali attributi del formato devono essere applicati alla tabella.

```csharp
public string FormatAttributes { get; set; }
```

## Esempi

Mostra come estrarre dati da un database e inserirli come campo in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Questo campo DATABASE eseguirà una query su un database e visualizzerà il risultato in una tabella.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Inserire un altro campo DATABASE con una query più complessa che ordina tutti i prodotti in ordine decrescente in base alle vendite lorde.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Queste proprietà hanno la stessa funzione delle clausole LIMIT e TOP.
// Configurarli per visualizzare solo le righe da 1 a 10 del risultato della query nella tabella del campo.
field.FirstRecord = "1";
field.LastRecord = "10";

// Questa proprietà è l'indice del formato che vogliamo utilizzare per la nostra tabella. L'elenco dei formati di tabella si trova nel menu "Formattazione automatica tabella..."
// che viene visualizzato quando creiamo un campo DATABASE in Microsoft Word. L'indice n. 10 corrisponde al formato "Colorful 3".
field.TableFormat = "10";

// La proprietà FormatAttribute è una rappresentazione stringa di un numero intero che memorizza più flag.
// Possiamo applicare patrimonialmente il formato a cui punta la proprietà TableFormat impostando flag diversi in questa proprietà.
// Il numero che utilizziamo è la somma di una combinazione di valori corrispondenti a diversi aspetti dello stile della tabella.
// 63 rappresenta 1 (bordi) + 2 (ombreggiatura) + 4 (carattere) + 8 (colore) + 16 (adattamento automatico) + 32 (righe di intestazione).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Guarda anche

* class [FieldDatabase](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
