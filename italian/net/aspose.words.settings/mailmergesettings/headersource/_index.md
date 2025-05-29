---
title: MailMergeSettings.HeaderSource
linktitle: HeaderSource
articleTitle: HeaderSource
second_title: Aspose.Words per .NET
description: Scopri la proprietà HeaderSource di MailMergeSettings e definisci il percorso dell'intestazione della tua stampa unione senza sforzo. Ottimizza il flusso di lavoro dei tuoi documenti oggi stesso!
type: docs
weight: 100
url: /it/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

Specifica il percorso alla sorgente dell'intestazione di stampa unione. Il valore predefinito è una stringa vuota.

```csharp
public string HeaderSource { get; set; }
```

## Esempi

Mostra come creare un'origine dati per una stampa unione a partire da un'origine intestazione e da un'origine dati.

```csharp
// Crea un file di intestazione per l'unione delle etichette di spedizione, che sarà composto da una tabella con una riga.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Crea un file di dati di unione delle etichette di spedizione costituito da una tabella con una riga
 // e lo stesso numero di colonne della tabella del documento di intestazione.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Crea un documento di destinazione di unione con MERGEFIELDS con nomi che
// abbina i nomi delle colonne nella tabella del file di intestazione di unione.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Costruiamo una fonte dati per la nostra stampa unione specificando due nomi di file di documento.
// L'origine dell'intestazione nominerà le colonne della tabella della sorgente dati.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// L'origine dati fornirà righe di dati per tutte le colonne nella tabella del documento di intestazione.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Configurare un tipo di etichetta di posta elettronica per la stampa unione, che verrà eseguita da Microsoft Word
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
