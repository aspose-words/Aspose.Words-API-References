---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words per .NET
description: Scopri ExactDateTimeParseFormats di JsonDataLoadOptions per un'analisi precisa delle date e degli orari JSON. Personalizza facilmente i formati per un caricamento dati impeccabile!
type: docs
weight: 30
url: /it/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Ottiene o imposta i formati esatti per l'analisi dei valori data-ora JSON durante il caricamento di JSON. Il valore predefinito è`null` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Osservazioni

Le stringhe codificate utilizzando il formato data-ora Microsoft® JSON (ad esempio, "/Date(1224043200000)/") vengono sempre riconosciute come valori data-ora, indipendentemente dal valore di questa proprietà. La proprietà definisce formati aggiuntivi da utilizzare durante l'analisi dei valori data-ora dalle stringhe nel modo seguente:

* Quando`ExactDateTimeParseFormats` È`null` , il formato ISO-8601 e tutti i formati data-ora supportati per le attuali culture inglese USA e inglese neozelandese vengono utilizzati inoltre nell'ordine menzionato.
* Quando`ExactDateTimeParseFormats`contiene stringhe, vengono utilizzate come formati date-time aggiuntivi utilizzando la cultura corrente.
* Quando`ExactDateTimeParseFormats` è vuoto, non vengono utilizzati formati data-ora aggiuntivi.

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
