---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Reporting.JsonSimpleValueParseMode per un parsing JSON efficiente. Gestisci facilmente valori nulli, booleani, numeri e stringhe senza problemi!
type: docs
weight: 5440
url: /it/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Specifica una modalità per l'analisi di valori JSON semplici (null, booleani, numeri, interi e stringhe) durante il caricamento di JSON. Tale modalità non influisce sull'analisi dei valori di data e ora.

```csharp
public enum JsonSimpleValueParseMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Loose | `0` | Specifica la modalità in cui i tipi di valori semplici JSON vengono determinati durante l'analisi delle loro rappresentazioni di stringa. Ad esempio, il tipo di 'prop' dallo snippet JSON '{ prop: "123" }' viene determinato come intero in questa modalità. |
| Strict | `1` | Specifica la modalità in cui i tipi di valori semplici JSON vengono determinati dalla notazione JSON stessa. Ad esempio, il tipo di 'prop' dallo snippet JSON '{ prop: "123" }' viene determinato come stringa in questa modalità. |

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
