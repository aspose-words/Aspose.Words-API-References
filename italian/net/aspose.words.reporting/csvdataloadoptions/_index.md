---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Reporting.CsvDataLoadOptions per un'analisi efficiente dei dati CSV. Ottimizza l'elaborazione dei tuoi documenti con opzioni personalizzabili oggi stesso!
type: docs
weight: 5400
url: /it/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

Rappresenta le opzioni per l'analisi dei dati CSV.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class CsvDataLoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Inizializza una nuova istanza di questa classe con opzioni predefinite. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | Inizializza una nuova istanza di questa classe specificando se i dati CSV contengono nomi di colonna nella prima riga. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | Ottiene o imposta il carattere utilizzato per commentare le righe di dati CSV. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Ottiene o imposta il carattere da utilizzare come delimitatore di colonna. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | Ottiene o imposta un valore che indica se il primo record di dati CSV contiene nomi di colonna. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Ottiene o imposta il carattere utilizzato per racchiudere tra virgolette i valori dei campi. |

## Osservazioni

Un'istanza di questa classe può essere passata ai costruttori di[`CsvDataSource`](../csvdatasource/) .

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

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
