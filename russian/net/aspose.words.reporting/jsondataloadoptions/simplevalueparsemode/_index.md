---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SimpleValueParseMode в JsonDataLoadOptions улучшает парсинг JSON для значений null, логических значений, чисел и строк. Оптимизируйте загрузку данных сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

Возвращает или задает режим для разбора простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. Такой режим не влияет на разбор значений даты и времени. Значение по умолчанию — Loose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
```

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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
