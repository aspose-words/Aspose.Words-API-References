---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: Aspose.Words per .NET
description: Scopri come personalizzare la proprietà CommentChar in CsvDataLoadOptions per migliorare la gestione dei dati CSV. Ottimizza il caricamento dei dati oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

Ottiene o imposta il carattere utilizzato per commentare le righe di dati CSV.

```csharp
public char CommentChar { get; set; }
```

## Osservazioni

Il valore predefinito è '#' (cancelletto).

## Esempi

Mostra come utilizzare CSV come origine dati (stringa).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Guarda anche

* class [CsvDataLoadOptions](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
