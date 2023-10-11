---
title: Class CsvDataSource
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Reporting.CsvDataSource сорт. Обеспечивает доступ к данным CSVфайла или потока которые будут использоваться в отчете.
type: docs
weight: 4670
url: /ru/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Обеспечивает доступ к данным CSV-файла или потока, которые будут использоваться в отчете.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) статья документации.

```csharp
public class CsvDataSource
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(Stream) | Создает новый источник данных с данными из потока CSV, используя параметры по умолчанию для анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(string) | Создает новый источник данных с данными из файла CSV, используя параметры по умолчанию для анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(Stream, CsvDataLoadOptions) | Создает новый источник данных с данными из потока CSV, используя указанные параметры анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(string, CsvDataLoadOptions) | Создает новый источник данных с данными из файла CSV, используя указанные параметры анализа данных CSV. |

### Примечания

Чтобы получить доступ к данным соответствующего файла или потока при создании отчета, передайте экземпляр этого класса как источник данных одному из[`ReportingEngine`](../reportingengine/) .BuildReport перегрузки.

В шаблонных документах`CsvDataSource` экземпляр следует рассматривать так же, как если бы он был aDataTable экземпляр . Для получения дополнительной информации см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

Типы данных значений, разделенных запятыми, определяются автоматически на основе их строкового представления. Таким образом, в документах template вы можете работать с типизированными значениями, а не только со строками. Движок способен автоматически распознавать значения следующих типов:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Обратите внимание, что для автоматического распознавания типов данных для работы строковые представления значений, разделенных запятыми, должны формироваться с использованием инвариантных настроек региональных параметров.

Чтобы переопределить поведение по умолчанию при загрузке данных CSV, инициализируйте и передайте[`CsvDataLoadOptions`](../csvdataloadoptions/) экземпляр в конструктор этого класса.

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)


