---
title: Class JsonDataLoadOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Reporting.JsonDataLoadOptions сорт. Представляет параметры анализа данных JSON.
type: docs
weight: 4680
url: /ru/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Представляет параметры анализа данных JSON.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) статья документации.

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
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Получает или задает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для элемента JSON root . Если корневой элемент JSON содержит одно сложное свойство, такой объект по умолчанию не создается. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Получает или задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. Значение по умолчанию:`нулевой` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Получает или задает флаг, указывающий, следует ли сохранять начальные и конечные пробелы при загрузке значений string данных JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Получает или задает режим анализа простых значений JSON (нулевое, логическое, число, целое число и строка) при загрузке JSON. Такой режим не влияет на анализ значений даты и времени. По умолчанию — .Loose . |

### Примечания

Экземпляр этого класса можно передать в конструкторы[`JsonDataSource`](../jsondatasource/) .

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)


