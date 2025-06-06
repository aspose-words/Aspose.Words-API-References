---
title: MailMergeSettings.HeaderSource
linktitle: HeaderSource
articleTitle: HeaderSource
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HeaderSource MailMergeSettings, определите путь заголовка слияния почты без усилий. Оптимизируйте свой документооборот сегодня!
type: docs
weight: 100
url: /ru/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

Указывает путь к источнику заголовка слияния почты. Значение по умолчанию — пустая строка.

```csharp
public string HeaderSource { get; set; }
```

## Примеры

Показывает, как создать источник данных для слияния почты из источника заголовка и источника данных.

```csharp
// Создайте файл заголовка слияния почтовых этикеток, который будет состоять из таблицы с одной строкой.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Создать файл данных слияния почтовых этикеток, состоящий из таблицы с одной строкой
 // и такое же количество столбцов, как и в таблице заголовочного документа.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Создать целевой документ слияния с MERGEFIELDS с именами, которые
// сопоставить имена столбцов в таблице файла заголовка слияния.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Создаем источник данных для нашего слияния, указав два имени файлов документов.
// Источник заголовка будет именовать столбцы таблицы источника данных.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Источник данных предоставит строки данных для всех столбцов в таблице документа заголовка.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Настройте тип почтовой метки для слияния писем, которое будет выполнять Microsoft Word
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
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
