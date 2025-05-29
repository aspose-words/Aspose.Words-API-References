---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words для .NET
description: Получайте доступ и используйте данные CSV без усилий с Aspose.Words.Reporting.CsvDataSource. Улучшайте свои отчеты с помощью бесшовной интеграции данных!
type: docs
weight: 5410
url: /ru/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Предоставляет доступ к данным CSV-файла или потока для использования в отчете.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) документальная статья.

```csharp
public class CsvDataSource
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Создает новый источник данных с данными из потока CSV, используя параметры по умолчанию для анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Создает новый источник данных с данными из CSV-файла, используя параметры по умолчанию для анализа CSV-данных. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Создает новый источник данных с данными из потока CSV, используя указанные параметры для анализа данных CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Создает новый источник данных с данными из CSV-файла, используя указанные параметры для анализа CSV-данных. |

## Примечания

Чтобы получить доступ к данным соответствующего файла или потока при формировании отчета, передайте экземпляр этого класса как источник данных одному из[`ReportingEngine`](../reportingengine/) .BuildReport перегрузки.

В шаблонах документов,`CsvDataSource` экземпляр следует обрабатывать так же, как если бы он был DataTableЭкземпляр . Для получения дополнительной информации см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Типы данных значений, разделенных запятыми, определяются автоматически по их строковым представлениям. Таким образом, в документах template вы можете работать с типизированными значениями, а не только со строками. Движок способен автоматически распознавать значения следующих типов:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Обратите внимание, что для работы автоматического распознавания типов данных строковые представления значений, разделенных запятыми, должны формироваться с использованием инвариантных настроек культуры.

Чтобы переопределить поведение по умолчанию при загрузке данных CSV, инициализируйте и передайте[`CsvDataLoadOptions`](../csvdataloadoptions/) instance в конструктор этого класса.

## Примеры

Показывает, как использовать CSV в качестве источника данных (строка).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
