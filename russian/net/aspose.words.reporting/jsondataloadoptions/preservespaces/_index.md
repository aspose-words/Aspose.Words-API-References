---
title: JsonDataLoadOptions.PreserveSpaces
linktitle: PreserveSpaces
articleTitle: PreserveSpaces
second_title: Aspose.Words для .NET
description: Узнайте, как свойство JsonDataLoadOptions PreserveSpaces улучшает обработку данных JSON, сохраняя начальные и конечные пробелы для точных строковых значений.
type: docs
weight: 40
url: /ru/net/aspose.words.reporting/jsondataloadoptions/preservespaces/
---
## JsonDataLoadOptions.PreserveSpaces property

Возвращает или задает флаг, указывающий, следует ли сохранять начальные и конечные пробелы при загрузке значений string данных JSON.

```csharp
public bool PreserveSpaces { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

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

* class [JsonDataLoadOptions](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
