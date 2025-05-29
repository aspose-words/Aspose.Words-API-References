---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Reporting.JsonSimpleValueParseMode для эффективного анализа JSON. Легко обрабатывайте null, логические значения, числа и строки!
type: docs
weight: 5440
url: /ru/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Указывает режим для анализа простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. Такой режим не влияет на анализ значений даты и времени.

```csharp
public enum JsonSimpleValueParseMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Loose | `0` | Указывает режим, в котором типы простых значений JSON определяются при анализе их строковых представлений. Например, тип 'prop' из фрагмента JSON '{ prop: "123" }' определяется как целое число в этом режиме. |
| Strict | `1` | Указывает режим, в котором типы простых значений JSON определяются из самой нотации JSON. Например, тип 'prop' из фрагмента JSON '{ prop: "123" }' определяется как строка в этом режиме. |

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

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
