---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words для .NET
description: Откройте для себя мощные отчеты с Aspose.Words.Reporting.JsonDataSource. Легкий доступ к данным JSON для бесшовной интеграции в ваши отчеты.
type: docs
weight: 5430
url: /ru/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Предоставляет доступ к данным файла JSON или потока для использования в отчете.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) документальная статья.

```csharp
public class JsonDataSource
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Создает новый источник данных с данными из потока JSON, используя параметры по умолчанию для анализа данных JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Создает новый источник данных с данными из файла JSON, используя параметры по умолчанию для анализа данных JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Создает новый источник данных с данными из потока JSON, используя указанные параметры для анализа данных JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Создает новый источник данных с данными из файла JSON, используя указанные параметры для анализа данных JSON. |

## Примечания

Чтобы получить доступ к данным соответствующего файла или потока при формировании отчета, передайте экземпляр этого класса как источник данных одному из[`ReportingEngine`](../reportingengine/) .BuildReport перегрузки.

В шаблонных документах, если элемент JSON верхнего уровня является массивом,`JsonDataSource` экземпляр должен be обрабатываться так же, как если бы это былDataTable экземпляр. Если элемент JSON верхнего уровня является объектом,`JsonDataSource` экземпляр следует обрабатывать так же, как если бы это был DataRow Экземпляр . Для получения дополнительной информации см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

В шаблонных документах можно работать с типизированными значениями элементов JSON. Для удобства движок заменяет набор простых типов JSON на следующий:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Движок автоматически распознает значения дополнительных типов по их JSON-представлениям.

Чтобы переопределить поведение по умолчанию при загрузке данных JSON, инициализируйте и передайте[`JsonDataLoadOptions`](../jsondataloadoptions/) instance в конструктор этого класса.

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
