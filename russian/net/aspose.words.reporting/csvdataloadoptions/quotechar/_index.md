---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CsvDataLoadOptions QuoteChar, позволяющее легко настраивать кавычки значений полей для бесперебойной обработки данных и улучшенного управления CSV.
type: docs
weight: 50
url: /ru/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

Возвращает или задает символ, который используется для заключения значений полей в кавычки.

```csharp
public char QuoteChar { get; set; }
```

## Примечания

Значение по умолчанию — '"' (кавычки).

Чтобы поместить символ в цитируемый текст, удвойте его.

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
