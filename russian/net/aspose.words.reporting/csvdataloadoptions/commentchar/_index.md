---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство CommentChar в CsvDataLoadOptions для улучшения обработки данных CSV. Оптимизируйте загрузку данных сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

Возвращает или задает символ, который используется для комментариев к строкам данных CSV.

```csharp
public char CommentChar { get; set; }
```

## Примечания

Значение по умолчанию — «#» (знак числа).

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
