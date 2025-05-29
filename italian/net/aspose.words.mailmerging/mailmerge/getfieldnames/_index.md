---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words per .NET
description: Scopri il metodo MailMerge GetFieldNames per accedere e utilizzare senza sforzo tutti i nomi dei campi di stampa unione nel tuo documento, per un'automazione semplificata dei documenti.
type: docs
weight: 220
url: /it/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Restituisce una raccolta di nomi di campi di unione di posta disponibili nel documento.

```csharp
public string[] GetFieldNames()
```

## Osservazioni

Restituisce i nomi completi dei campi unione, incluso il prefisso facoltativo. Non elimina i nomi di campo duplicati.

A ogni chiamata viene creato un nuovo array di stringhe.

Include i nomi dei campi "baffi" se[`UseNonMergeFields`](../usenonmergefields/) È`VERO`.

## Esempi

Mostra come ottenere i nomi di tutti i campi di unione in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// Per ogni nome MERGEFIELD nel documento, assicurarsi che la tabella dati contenga una colonna
 // con lo stesso nome, quindi eseguire la stampa unione.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
