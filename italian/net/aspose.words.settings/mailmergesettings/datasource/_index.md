---
title: MailMergeSettings.DataSource
linktitle: DataSource
articleTitle: DataSource
second_title: Aspose.Words per .NET
description: MailMergeSettings DataSource proprietà. Specifica il percorso dellorigine dati di stampa unione. Il valore predefinito è una stringa vuota in C#.
type: docs
weight: 60
url: /it/net/aspose.words.settings/mailmergesettings/datasource/
---
## MailMergeSettings.DataSource property

Specifica il percorso dell'origine dati di stampa unione. Il valore predefinito è una stringa vuota.

```csharp
public string DataSource { get; set; }
```

## Esempi

Mostra come costruire un'origine dati per una stampa unione da un'origine intestazione e un'origine dati.

```csharp
// Crea un file di intestazione di unione delle etichette postali, che consisterà in una tabella con una riga.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Crea un file di dati di unione di etichette postali costituito da una tabella con una riga
 // e lo stesso numero di colonne della tabella dell'intestazione del documento.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Crea un documento di destinazione dell'unione con MERGEFIELDS con i nomi that
// abbina i nomi delle colonne nella tabella del file di intestazione dell'unione.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Costruisce un'origine dati per la nostra stampa unione specificando due nomi di file di documento.
// L'origine dell'intestazione nominerà le colonne della tabella dell'origine dati.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// L'origine dati fornirà righe di dati per tutte le colonne nella tabella dei documenti dell'intestazione.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Configura una stampa unione di tipo etichetta postale, che verrà eseguita da Microsoft Word
// non appena lo utilizziamo per caricare il documento di output.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Guarda anche

* class [MailMergeSettings](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
