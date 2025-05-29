---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words для .NET
description: Откройте для себя ExactDateTimeParseFormats JsonDataLoadOptions для точного анализа даты и времени в формате JSON. Легко настраивайте форматы для бесперебойной загрузки данных!
type: docs
weight: 30
url: /ru/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Получает или задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. Значение по умолчанию`нулевой` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Примечания

Строки, закодированные с использованием формата даты и времени Microsoft® JSON (например, "/Date(1224043200000)/"), всегда распознаются как значения даты и времени независимо от значения этого свойства. Свойство определяет дополнительные форматы , которые следует использовать при разборе значений даты и времени из строк следующим образом:

* Когда`ExactDateTimeParseFormats` является`нулевой` , формат ISO-8601 и все форматы даты и времени , поддерживаемые для текущей культуры, английской (США) и английской (Новая Зеландия), используются дополнительно в указанном порядке.
* Когда`ExactDateTimeParseFormats`содержит строки, они используются как дополнительные форматы даты-времени , использующие текущую культуру.
* Когда`ExactDateTimeParseFormats` пусто, дополнительные форматы даты и времени не используются.

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
