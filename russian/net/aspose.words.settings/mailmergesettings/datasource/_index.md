---
title: MailMergeSettings.DataSource
second_title: Справочник по API Aspose.Words для .NET
description: MailMergeSettings свойство. Указывает путь к источнику данных слияния почты. Значение по умолчанию  пустая строка.
type: docs
weight: 60
url: /ru/net/aspose.words.settings/mailmergesettings/datasource/
---
## MailMergeSettings.DataSource property

Указывает путь к источнику данных слияния почты. Значение по умолчанию — пустая строка.

```csharp
public string DataSource { get; set; }
```

### Примеры

Показывает, как создать источник данных для слияния почты из источника заголовка и источника данных.

```csharp
// Создаем файл заголовка слияния почтовой метки, который будет состоять из таблицы с одной строкой.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Создаем файл данных слияния почтовой метки, состоящий из таблицы с одной строкой
 // и такое же количество столбцов, как и в таблице заголовка документа.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Создание целевого документа слияния с MERGEFIELDS с именами, которые
// сопоставляем имена столбцов в таблице файла заголовка слияния.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Создайте источник данных для нашего слияния почты, указав два имени файла документа.
// Источник заголовка будет называть столбцы таблицы источника данных.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Источник данных предоставит строки данных для всех столбцов таблицы заголовка документа.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Настраиваем слияние писем типа почтовой метки, которое будет выполнять Microsoft Word
// как только мы используем его для загрузки выходного документа.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Смотрите также

* class [MailMergeSettings](../)
* пространство имен [Aspose.Words.Settings](../../mailmergesettings/)
* сборка [Aspose.Words](../../../)


