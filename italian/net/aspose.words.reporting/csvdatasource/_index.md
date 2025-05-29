---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words per .NET
description: Accedi e utilizza i dati CSV senza sforzo con Aspose.Words.Reporting.CsvDataSource. Migliora i tuoi report con un'integrazione dati perfetta!
type: docs
weight: 5410
url: /it/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Fornisce l'accesso ai dati di un file CSV o di un flusso da utilizzare in un report.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class CsvDataSource
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Crea una nuova origine dati con dati da un flusso CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Crea una nuova origine dati con dati da un file CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crea una nuova origine dati con dati da un flusso CSV utilizzando le opzioni specificate per l'analisi dei dati CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crea una nuova origine dati con dati da un file CSV utilizzando le opzioni specificate per l'analisi dei dati CSV. |

## Osservazioni

Per accedere ai dati del file o del flusso corrispondente durante la generazione di un report, passare un'istanza di questa classe come una fonte dati a uno dei[`ReportingEngine`](../reportingengine/) Sovraccarichi di .BuildReport.

Nei documenti modello, un`CsvDataSource` l'istanza dovrebbe essere trattata allo stesso modo come se fosse unDataTableIstanza . Per ulteriori informazioni, consultare il riferimento alla sintassi del template (https://docs.aspose.com/display/wordsnet/Template+Syntax).

I tipi di dati dei valori separati da virgole vengono determinati automaticamente in base alle loro rappresentazioni di stringa. Pertanto, nei documenti template , è possibile lavorare con valori tipizzati anziché solo con stringhe. Il motore è in grado di riconoscere automaticamente i valori dei seguenti tipi:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Si noti che affinché il riconoscimento automatico dei tipi di dati funzioni, le rappresentazioni di stringa dei valori separati da virgole devono essere formate utilizzando impostazioni di cultura invarianti.

Per sovrascrivere il comportamento predefinito del caricamento dei dati CSV, inizializzare e passare un[`CsvDataLoadOptions`](../csvdataloadoptions/) instance a un costruttore di questa classe.

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
