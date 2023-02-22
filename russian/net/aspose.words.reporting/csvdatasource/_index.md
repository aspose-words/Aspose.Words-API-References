---
title: Class CsvDataSource
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Reporting.CsvDataSource сорт. Предоставляет доступ к данным CSVфайла или потока для использования в отчете.
type: docs
weight: 4410
url: /ru/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Предоставляет доступ к данным CSV-файла или потока для использования в отчете.

```csharp
public class CsvDataSource
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(Stream) | Создает новый источник данных с данными из потока CSV, используя параметры по умолчанию для анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(string) | Создает новый источник данных с данными из файла CSV, используя параметры по умолчанию для анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(Stream, CsvDataLoadOptions) | Создает новый источник данных с данными из потока CSV, используя указанные параметры анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(string, CsvDataLoadOptions) | Создает новый источник данных с данными из CSV-файла, используя указанные параметры анализа CSV-данных. |

### Примечания

Чтобы получить доступ к данным соответствующего файла или потока при создании отчета, передайте экземпляр этого класса как источник данных одному из[`ReportingEngine`](../reportingengine/) Перегрузки .BuildReport.

В шаблонных документах`CsvDataSource` Экземпляр следует рассматривать так же, как если бы он был aDataTable экземпляр . Дополнительные сведения см. в справочнике по синтаксису шаблона (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Типы данных значений, разделенных запятыми, определяются автоматически при их строковом представлении. Таким образом, в документах template вы можете работать с типизированными значениями, а не только со строками. Движок способен автоматически распознавать значения следующих типов:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Обратите внимание, что для работы автоматического распознавания типов данных строковые представления значений, разделенных запятыми, должны формироваться с использованием инвариантных настроек культуры.

Чтобы переопределить поведение загрузки данных CSV по умолчанию, инициализируйте и передайте[`CsvDataLoadOptions`](../csvdataloadoptions/)instance в конструктор этого класса.

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)


