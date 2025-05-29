---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words для .NET
description: Создавайте мощные источники данных CSV без усилий с помощью нашего конструктора CsvDataSource. Упростите анализ данных с помощью параметров по умолчанию для бесшовной интеграции.
type: docs
weight: 10
url: /ru/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Создает новый источник данных с данными из CSV-файла, используя параметры по умолчанию для анализа CSV-данных.

```csharp
public CsvDataSource(string csvPath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvPath | String | Путь к CSV-файлу, который будет использоваться в качестве источника данных. |

### Смотрите также

* class [CsvDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Создает новый источник данных с данными из CSV-файла, используя указанные параметры для анализа CSV-данных.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvPath | String | Путь к CSV-файлу, который будет использоваться в качестве источника данных. |
| options | CsvDataLoadOptions | Варианты анализа данных CSV. |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Создает новый источник данных с данными из потока CSV, используя параметры по умолчанию для анализа данных CSV.

```csharp
public CsvDataSource(Stream csvStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvStream | Stream | Поток данных CSV, который будет использоваться в качестве источника данных. |

### Смотрите также

* class [CsvDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Создает новый источник данных с данными из потока CSV, используя указанные параметры для анализа данных CSV.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvStream | Stream | Поток данных CSV, который будет использоваться в качестве источника данных. |
| options | CsvDataLoadOptions | Варианты анализа данных CSV. |

## Примеры

Показывает, как использовать CSV в качестве источника данных (потока).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### Смотрите также

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
