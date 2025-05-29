---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words per .NET
description: Scopri la proprietà QuoteChar di CsvDataLoadOptions per personalizzare facilmente la quotazione dei valori dei campi per una gestione dei dati ottimale e una migliore gestione dei CSV.
type: docs
weight: 50
url: /it/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

Ottiene o imposta il carattere utilizzato per racchiudere tra virgolette i valori dei campi.

```csharp
public char QuoteChar { get; set; }
```

## Osservazioni

Il valore predefinito è '"' (virgolette).

Raddoppia il carattere per inserirlo nel testo tra virgolette.

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
