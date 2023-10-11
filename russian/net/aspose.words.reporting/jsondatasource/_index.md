---
title: Class JsonDataSource
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Reporting.JsonDataSource сорт. Обеспечивает доступ к данным файла или потока JSON которые будут использоваться в отчете.
type: docs
weight: 4690
url: /ru/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Обеспечивает доступ к данным файла или потока JSON, которые будут использоваться в отчете.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) статья документации.

```csharp
public class JsonDataSource
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | Создает новый источник данных с данными из потока JSON, используя параметры по умолчанию для анализа данных JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | Создает новый источник данных с данными из файла JSON, используя параметры по умолчанию для анализа данных JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | Создает новый источник данных с данными из потока JSON, используя указанные параметры анализа данных JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | Создает новый источник данных с данными из файла JSON, используя указанные параметры анализа данных JSON. |

### Примечания

Чтобы получить доступ к данным соответствующего файла или потока при создании отчета, передайте экземпляр этого класса как источник данных одному из[`ReportingEngine`](../reportingengine/) .BuildReport перегрузки.

В документах шаблонов, если элемент JSON верхнего уровня является массивом,`JsonDataSource` экземпляр be следует рассматривать так же, как если бы он былDataTable экземпляр . Если элемент JSON верхнего уровня является объектом,`JsonDataSource` экземпляр следует рассматривать так же, как если бы он был aDataRow экземпляр . Для получения дополнительной информации см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

В шаблонных документах можно работать с типизированными значениями элементов JSON. Для удобства движок заменяет набор простых типов JSON на следующий:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Механизм автоматически распознает значения дополнительных типов по их представлениям JSON.

Чтобы переопределить поведение по умолчанию при загрузке данных JSON, инициализируйте и передайте[`JsonDataLoadOptions`](../jsondataloadoptions/) экземпляр в конструктор этого класса.

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)


