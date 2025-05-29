---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SimpleValueParseMode in JsonDataLoadOptions migliora l'analisi JSON per valori nulli, booleani, numeri e stringhe. Ottimizza il caricamento dei tuoi dati oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

Ottiene o imposta una modalità per l'analisi di valori JSON semplici (null, booleani, numeri, interi e stringhe) durante il caricamento di JSON. Tale modalità non influisce sull'analisi dei valori di data e ora. Il valore predefinito è Loose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
