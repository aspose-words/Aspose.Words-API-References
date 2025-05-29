---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Reporting.JsonDataLoadOptions для бесшовного анализа данных JSON. Улучшите обработку документов с помощью гибких опций!
type: docs
weight: 5420
url: /ru/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Представляет параметры для анализа данных JSON.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) документальная статья.

```csharp
public class JsonDataLoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Инициализирует новый экземпляр этого класса с параметрами по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Возвращает или задает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для элемента JSON root . Если корневой элемент JSON содержит одно сложное свойство, такой объект по умолчанию не создается. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Получает или задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. Значение по умолчанию`нулевой` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Возвращает или задает флаг, указывающий, следует ли сохранять начальные и конечные пробелы при загрузке значений string данных JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Возвращает или задает режим для разбора простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. Такой режим не влияет на разбор значений даты и времени. Значение по умолчанию — Loose . |

## Примечания

Экземпляр этого класса может быть передан в конструкторы[`JsonDataSource`](../jsondatasource/) .

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
