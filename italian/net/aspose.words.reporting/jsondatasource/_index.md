---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words per .NET
description: Sblocca potenti funzionalità di reporting con Aspose.Words.Reporting.JsonDataSource. Accedi facilmente ai dati JSON per una perfetta integrazione nei tuoi report.
type: docs
weight: 5430
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
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Crea una nuova origine dati con dati da un flusso JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Crea una nuova origine dati con dati da un file JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crea una nuova origine dati con dati da un flusso JSON utilizzando le opzioni specificate per l'analisi dei dati JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crea una nuova origine dati con dati da un file JSON utilizzando le opzioni specificate per l'analisi dei dati JSON. |

## Osservazioni

Per accedere ai dati del file o del flusso corrispondente durante la generazione di un report, passare un'istanza di questa classe come una fonte dati a uno dei[`ReportingEngine`](../reportingengine/) Sovraccarichi di .BuildReport.

Nei documenti modello, se un elemento JSON di primo livello è un array, un`JsonDataSource` l'istanza dovrebbe essere trattata allo stesso modo come se fosse unDataTableIstanza . Se un elemento JSON di primo livello è un oggetto, un`JsonDataSource` l'istanza dovrebbe essere trattata allo stesso modo come se fosse aDataRow Istanza . Per ulteriori informazioni, consultare il riferimento alla sintassi del template (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Nei documenti modello, è possibile lavorare con valori tipizzati di elementi JSON. Per comodità, il motore sostituisce l'insieme di tipi semplici JSON con il seguente:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Il motore riconosce automaticamente i valori dei tipi extra nelle loro rappresentazioni JSON.

Per sovrascrivere il comportamento predefinito del caricamento dei dati JSON, inizializzare e passare un[`JsonDataLoadOptions`](../jsondataloadoptions/) instance a un costruttore di questa classe.

## Esempi

Mostra come utilizzare JSON come origine dati (stringa).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
