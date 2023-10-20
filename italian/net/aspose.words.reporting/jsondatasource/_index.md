---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words per .NET
description: Aspose.Words.Reporting.JsonDataSource classe. Fornisce laccesso ai dati di un file o flusso JSON da utilizzare allinterno di un report in C#.
type: docs
weight: 4690
url: /it/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Fornisce l'accesso ai dati di un file o flusso JSON da utilizzare all'interno di un report.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class JsonDataSource
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Crea una nuova origine dati con i dati di un flusso JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Crea una nuova origine dati con i dati di un file JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crea una nuova origine dati con i dati da un flusso JSON utilizzando le opzioni specificate per l'analisi dei dati JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crea una nuova origine dati con i dati di un file JSON utilizzando le opzioni specificate per l'analisi dei dati JSON. |

## Osservazioni

Per accedere ai dati del file o del flusso corrispondente durante la generazione di un report, passa un'istanza di questa classe come un'origine dati a uno dei[`ReportingEngine`](../reportingengine/) .BuildReport sovraccarichi.

Nei documenti modello, se un elemento JSON di livello superiore è un array, a`JsonDataSource` l'istanza dovrebbe essere trattata allo stesso modo come se fosse un fileDataTable istanza. Se un elemento JSON di livello superiore è un oggetto, a`JsonDataSource` l'istanza dovrebbe essere trattata come se fosse aDataRow istanza. Per ulteriori informazioni, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Nei documenti modello, puoi lavorare con valori digitati di elementi JSON. Per comodità, il motore sostituisce il set di tipi semplici JSON con il seguente:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Il motore riconosce automaticamente i valori dei tipi extra in base alle loro rappresentazioni JSON.

Per sovrascrivere il comportamento predefinito del caricamento dei dati JSON, inizializzare e passare a[`JsonDataLoadOptions`](../jsondataloadoptions/) istanza a un costruttore di questa classe.

### Guarda anche

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
