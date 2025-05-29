---
title: JsonDataLoadOptions.PreserveSpaces
linktitle: PreserveSpaces
articleTitle: PreserveSpaces
second_title: Aspose.Words per .NET
description: Scopri come la proprietà PreserveSpaces di JsonDataLoadOptions migliora la gestione dei dati JSON conservando gli spazi iniziali e finali per ottenere valori stringa accurati.
type: docs
weight: 40
url: /it/net/aspose.words.reporting/jsondataloadoptions/preservespaces/
---
## JsonDataLoadOptions.PreserveSpaces property

Ottiene o imposta un flag che indica se gli spazi iniziali e finali devono essere conservati durante il caricamento dei valori string dei dati JSON.

```csharp
public bool PreserveSpaces { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

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

* class [JsonDataLoadOptions](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
