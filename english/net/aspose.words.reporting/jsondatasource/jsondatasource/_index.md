---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words for .NET
description: Create a powerful data source effortlessly with the JsonDataSource constructor, enabling seamless integration of JSON files and optimized data parsing.
type: docs
weight: 10
url: /net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Creates a new data source with data from a JSON file using default options for parsing JSON data.

```csharp
public JsonDataSource(string jsonPath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| jsonPath | String | The path to the JSON file to be used as the data source. |

### See Also

* class [JsonDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Creates a new data source with data from a JSON stream using default options for parsing JSON data.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| jsonStream | Stream | The stream of JSON data to be used as the data source. |

### See Also

* class [JsonDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Creates a new data source with data from a JSON file using the specified options for parsing JSON data.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| jsonPath | String | The path to the JSON file to be used as the data source. |
| options | JsonDataLoadOptions | Options for parsing JSON data. |

## Examples

Shows how to use JSON as a data source (string).

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

### See Also

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Creates a new data source with data from a JSON stream using the specified options for parsing JSON data.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| jsonStream | Stream | The stream of JSON data to be used as the data source. |
| options | JsonDataLoadOptions | Options for parsing JSON data. |

## Examples

Shows how to use JSON as a data source (stream).

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

### See Also

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
