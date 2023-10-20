---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words per .NET
description: Aspose.Words.Reporting.CsvDataSource classe. Fornisce laccesso ai dati di un file CSV o di un flusso da utilizzare allinterno di un report in C#.
type: docs
weight: 4670
url: /it/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Fornisce l'accesso ai dati di un file CSV o di un flusso da utilizzare all'interno di un report.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class CsvDataSource
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Crea una nuova origine dati con i dati di un flusso CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Crea una nuova origine dati con i dati di un file CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crea una nuova origine dati con i dati da un flusso CSV utilizzando le opzioni specificate per l'analisi dei dati CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crea una nuova origine dati con i dati di un file CSV utilizzando le opzioni specificate per l'analisi dei dati CSV. |

## Osservazioni

Per accedere ai dati del file o del flusso corrispondente durante la generazione di un report, passa un'istanza di questa classe come un'origine dati a uno dei[`ReportingEngine`](../reportingengine/) .BuildReport sovraccarichi.

Nei documenti modello, a`CsvDataSource` l'istanza dovrebbe essere trattata come se fosse aDataTable istanza. Per ulteriori informazioni, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

I tipi di dati con valori separati da virgole vengono determinati automaticamente in base alle rappresentazioni di stringa. Quindi nei documenti template puoi lavorare con valori digitati anziché solo con stringhe. Il motore è in grado di riconoscere automaticamente valori dei seguenti tipi:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Tieni presente che affinché il riconoscimento automatico dei tipi di dati funzioni, le rappresentazioni di stringhe di valori separati da virgole devono essere formate utilizzando impostazioni cultura invarianti.

Per sovrascrivere il comportamento predefinito del caricamento dei dati CSV, inizializzare e passare a[`CsvDataLoadOptions`](../csvdataloadoptions/) istanza a un costruttore di questa classe.

### Guarda anche

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
