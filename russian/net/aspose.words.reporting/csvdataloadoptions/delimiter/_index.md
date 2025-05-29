---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CsvDataLoadOptions Delimiter, чтобы легко настраивать разделители столбцов для эффективной загрузки данных. Оптимизируйте управление данными сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Возвращает или задает символ, который будет использоваться в качестве разделителя столбцов.

```csharp
public char Delimiter { get; set; }
```

## Примечания

Значение по умолчанию — ',' (запятая).

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

* class [CsvDataLoadOptions](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
