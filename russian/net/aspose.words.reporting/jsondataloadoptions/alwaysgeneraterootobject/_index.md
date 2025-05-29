---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words для .NET
description: Узнайте, как свойство JsonDataLoadOptions AlwaysGenerateRootObject улучшает обработку данных JSON, обеспечивая согласованный корневой объект для бесшовной интеграции.
type: docs
weight: 20
url: /ru/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

Возвращает или задает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для элемента JSON root . Если корневой элемент JSON содержит одно сложное свойство, такой объект по умолчанию не создается.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
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
