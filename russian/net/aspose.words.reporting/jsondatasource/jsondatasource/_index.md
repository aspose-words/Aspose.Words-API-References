---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words для .NET
description: Создавайте мощные источники данных без особых усилий с помощью конструктора JsonDataSource, обеспечивающего бесшовную интеграцию файлов JSON и оптимизированный анализ данных.
type: docs
weight: 10
url: /ru/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

Создает новый источник данных с данными из файла JSON, используя параметры по умолчанию для анализа данных JSON.

```csharp
public JsonDataSource(string jsonPath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonPath | String | Путь к файлу JSON, который будет использоваться в качестве источника данных. |

### Смотрите также

* class [JsonDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

Создает новый источник данных с данными из потока JSON, используя параметры по умолчанию для анализа данных JSON.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonStream | Stream | Поток данных JSON, который будет использоваться в качестве источника данных. |

### Смотрите также

* class [JsonDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

Создает новый источник данных с данными из файла JSON, используя указанные параметры для анализа данных JSON.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonPath | String | Путь к файлу JSON, который будет использоваться в качестве источника данных. |
| options | JsonDataLoadOptions | Варианты анализа данных JSON. |

## Примеры

Показывает, как использовать JSON в качестве источника данных (строки).

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

### Смотрите также

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

Создает новый источник данных с данными из потока JSON, используя указанные параметры для анализа данных JSON.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonStream | Stream | Поток данных JSON, который будет использоваться в качестве источника данных. |
| options | JsonDataLoadOptions | Варианты анализа данных JSON. |

## Примеры

Показывает, как использовать JSON в качестве источника данных (потока).

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

### Смотрите также

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
