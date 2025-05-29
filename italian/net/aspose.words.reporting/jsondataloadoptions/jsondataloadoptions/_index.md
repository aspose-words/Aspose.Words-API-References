---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore JsonDataLoadOptions e inizializza senza sforzo il caricamento dei dati con impostazioni predefinite personalizzabili per prestazioni ottimali.
type: docs
weight: 10
url: /it/net/aspose.words.reporting/jsondataloadoptions/jsondataloadoptions/
---
## JsonDataLoadOptions constructor

Inizializza una nuova istanza di questa classe con opzioni predefinite.

```csharp
public JsonDataLoadOptions()
```

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
