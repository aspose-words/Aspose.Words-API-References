---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HasHeaders класса CsvDataLoadOptions, чтобы легко управлять импортом CSV, указывая, содержит ли первая запись имена столбцов для бесшовной интеграции данных.
type: docs
weight: 40
url: /ru/net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

Возвращает или задает значение, указывающее, содержит ли первая запись данных CSV имена столбцов.

```csharp
public bool HasHeaders { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

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
