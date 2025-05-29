---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Reporting.CsvDataLoadOptions для эффективного анализа данных CSV. Оптимизируйте обработку документов с помощью настраиваемых параметров уже сегодня!
type: docs
weight: 5400
url: /ru/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

Представляет параметры для анализа данных CSV.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) документальная статья.

```csharp
public class CsvDataLoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Инициализирует новый экземпляр этого класса с параметрами по умолчанию. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | Инициализирует новый экземпляр этого класса, указывая, содержат ли данные CSV имена столбцов в первой строке. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | Возвращает или задает символ, который используется для комментариев к строкам данных CSV. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Возвращает или задает символ, который будет использоваться в качестве разделителя столбцов. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | Возвращает или задает значение, указывающее, содержит ли первая запись данных CSV имена столбцов. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Возвращает или задает символ, который используется для заключения значений полей в кавычки. |

## Примечания

Экземпляр этого класса может быть передан в конструкторы[`CsvDataSource`](../csvdatasource/) .

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
