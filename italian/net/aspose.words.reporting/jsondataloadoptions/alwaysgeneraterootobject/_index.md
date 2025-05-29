---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words per .NET
description: Scopri come la proprietà AlwaysGenerateRootObject di JsonDataLoadOptions migliora la gestione dei dati JSON garantendo un oggetto radice coerente per un'integrazione perfetta.
type: docs
weight: 20
url: /it/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

Ottiene o imposta un flag che indica se un'origine dati generata conterrà sempre un oggetto per un elemento JSON root . Se un elemento JSON root contiene una singola proprietà complessa, tale oggetto non viene creato per impostazione predefinita.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
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
