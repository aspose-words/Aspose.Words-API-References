---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words para .NET
description: Cree una fuente de datos poderosa sin esfuerzo con el constructor JsonDataSource, que permite una integración perfecta de archivos JSON y un análisis de datos optimizado.
type: docs
weight: 10
url: /es/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Crea una nueva fuente de datos con datos de un archivo JSON utilizando las opciones predeterminadas para analizar datos JSON.

```csharp
public JsonDataSource(string jsonPath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| jsonPath | String | La ruta al archivo JSON que se utilizará como fuente de datos. |

### Ver también

* class [JsonDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Crea una nueva fuente de datos con datos de una secuencia JSON utilizando las opciones predeterminadas para analizar datos JSON.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| jsonStream | Stream | El flujo de datos JSON que se utilizará como fuente de datos. |

### Ver también

* class [JsonDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Crea una nueva fuente de datos con datos de un archivo JSON utilizando las opciones especificadas para analizar datos JSON.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| jsonPath | String | La ruta al archivo JSON que se utilizará como fuente de datos. |
| options | JsonDataLoadOptions | Opciones para analizar datos JSON. |

## Ejemplos

Muestra cómo utilizar JSON como fuente de datos (cadena).

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

### Ver también

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Crea una nueva fuente de datos con datos de una secuencia JSON utilizando las opciones especificadas para analizar datos JSON.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| jsonStream | Stream | El flujo de datos JSON que se utilizará como fuente de datos. |
| options | JsonDataLoadOptions | Opciones para analizar datos JSON. |

## Ejemplos

Muestra cómo utilizar JSON como fuente de datos (flujo).

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

### Ver también

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
