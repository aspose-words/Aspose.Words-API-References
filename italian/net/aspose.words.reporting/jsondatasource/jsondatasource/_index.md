---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words per .NET
description: Crea senza sforzo una potente fonte di dati con il costruttore JsonDataSource, consentendo un'integrazione perfetta dei file JSON e un'analisi ottimizzata dei dati.
type: docs
weight: 10
url: /it/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Crea una nuova origine dati con dati da un file JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON.

```csharp
public JsonDataSource(string jsonPath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonPath | String | Percorso al file JSON da utilizzare come origine dati. |

### Guarda anche

* class [JsonDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Crea una nuova origine dati con dati da un flusso JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonStream | Stream | Flusso di dati JSON da utilizzare come origine dati. |

### Guarda anche

* class [JsonDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Crea una nuova origine dati con dati da un file JSON utilizzando le opzioni specificate per l'analisi dei dati JSON.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonPath | String | Percorso al file JSON da utilizzare come origine dati. |
| options | JsonDataLoadOptions | Opzioni per l'analisi dei dati JSON. |

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

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Crea una nuova origine dati con dati da un flusso JSON utilizzando le opzioni specificate per l'analisi dei dati JSON.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonStream | Stream | Flusso di dati JSON da utilizzare come origine dati. |
| options | JsonDataLoadOptions | Opzioni per l'analisi dei dati JSON. |

## Esempi

Mostra come utilizzare JSON come origine dati (flusso).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"}
};

using (FileStream stream = File.OpenRead(MyDir + "List of people.json"))
{
    JsonDataSource dataSource = new JsonDataSource(stream, options);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataStream.docx");
```

### Guarda anche

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
