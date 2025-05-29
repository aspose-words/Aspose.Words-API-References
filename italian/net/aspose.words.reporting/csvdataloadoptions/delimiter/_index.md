---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words per .NET
description: Scopri la proprietà Delimitatore di CsvDataLoadOptions per personalizzare facilmente i delimitatori di colonna per un caricamento dati efficiente. Ottimizza la gestione dei tuoi dati oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Ottiene o imposta il carattere da utilizzare come delimitatore di colonna.

```csharp
public char Delimiter { get; set; }
```

## Osservazioni

Il valore predefinito è ',' (virgola).

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
