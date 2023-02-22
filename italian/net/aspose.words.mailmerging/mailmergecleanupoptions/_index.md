---
title: Enum MailMergeCleanupOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.MailMerging.MailMergeCleanupOptions enum. Specifica le opzioni che determinano quali elementi vengono rimossi durante la stampa unione.
type: docs
weight: 3630
url: /it/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Specifica le opzioni che determinano quali elementi vengono rimossi durante la stampa unione.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Specifica un valore predefinito. |
| RemoveEmptyParagraphs | `1` | Specifica se i paragrafi che contenevano campi di stampa unione senza dati devono essere rimossi dal documento. Quando questa opzione è impostata, vengono rimossi anche i paragrafi che contengono campi di inizio e fine area di unione che altrimenti sarebbero vuoti . |
| RemoveUnusedRegions | `2` | Specifica se le aree di stampa unione non utilizzate devono essere rimosse dal documento. |
| RemoveUnusedFields | `4` | Specifica se i campi di unione inutilizzati devono essere rimossi dal documento. |
| RemoveContainingFields | `8` | Specifica se i campi che contengono campi di unione (ad esempio, IF) devono essere rimossi dal documento se i campi di unione nidificati vengono rimossi. |
| RemoveStaticFields | `10` | Specifica se i campi statici devono essere rimossi dal documento. I campi statici sono campi i cui risultati rimangono gli stessi a qualsiasi modifica del documento. I campi, che non memorizzano i risultati in un documento e vengono calcolati al volo (comeFieldListNum , FieldSymbol , ecc.) non sono considerati statici. |
| RemoveEmptyTableRows | `20` | Specifica se le righe vuote che contengono aree di stampa unione devono essere rimosse dal documento. |

### Esempi

Mostra come rimuovere i paragrafi vuoti che una stampa unione può creare dal documento di output dell'unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

Mostra come rimuovere automaticamente i MERGEFIELD che restano inutilizzati durante la stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un documento con MERGEFIELD per tre colonne di una tabella di origine dati stampa unione,
// e quindi crea una tabella con solo due colonne i cui nomi corrispondono ai nostri MERGEFIELD.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// Il nostro terzo MERGEFIELD fa riferimento a una colonna "Città", che non esiste nella nostra origine dati.
// La stampa unione lascerà intatti campi come questo nel loro stato precedente all'unione.
// L'impostazione della proprietà "CleanupOptions" su "RemoveUnusedFields" rimuoverà tutti i MERGEFIELD
// che non vengono utilizzati durante una stampa unione per ripulire i documenti di unione.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)


