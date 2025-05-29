---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Reporting.JsonDataLoadOptions per un'analisi fluida dei dati JSON. Migliora l'elaborazione dei tuoi documenti con opzioni flessibili!
type: docs
weight: 5420
url: /it/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Rappresenta le opzioni per l'analisi dei dati JSON.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class JsonDataLoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Inizializza una nuova istanza di questa classe con opzioni predefinite. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Ottiene o imposta un flag che indica se un'origine dati generata conterrà sempre un oggetto per un elemento JSON root . Se un elemento JSON root contiene una singola proprietà complessa, tale oggetto non viene creato per impostazione predefinita. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Ottiene o imposta i formati esatti per l'analisi dei valori data-ora JSON durante il caricamento di JSON. Il valore predefinito è`null` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Ottiene o imposta un flag che indica se gli spazi iniziali e finali devono essere conservati durante il caricamento dei valori string dei dati JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Ottiene o imposta una modalità per l'analisi di valori JSON semplici (null, booleani, numeri, interi e stringhe) durante il caricamento di JSON. Tale modalità non influisce sull'analisi dei valori di data e ora. Il valore predefinito è Loose . |

## Osservazioni

Un'istanza di questa classe può essere passata ai costruttori di[`JsonDataSource`](../jsondatasource/) .

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
