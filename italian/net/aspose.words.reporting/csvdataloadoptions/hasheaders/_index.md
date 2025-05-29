---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: Aspose.Words per .NET
description: Scopri la proprietà HasHeaders di CsvDataLoadOptions per gestire facilmente le importazioni CSV specificando se il primo record include nomi di colonna per un'integrazione dati ottimale.
type: docs
weight: 40
url: /it/net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

Ottiene o imposta un valore che indica se il primo record di dati CSV contiene nomi di colonna.

```csharp
public bool HasHeaders { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

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
