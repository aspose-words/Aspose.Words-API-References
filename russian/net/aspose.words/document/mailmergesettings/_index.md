---
title: Document.MailMergeSettings
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или задает объект содержащий всю информацию о слиянии для документа.
type: docs
weight: 250
url: /ru/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Получает или задает объект, содержащий всю информацию о слиянии для документа.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

### Примечания

Вы можете использовать этот объект, чтобы указать источник данных слияния для документа, и эта информация (вместе с доступными полями данных) появится в Microsoft Word, когда пользователь откроет этот документ. Или вы можете использовать этот объект для запроса настроек слияния почты. который пользователь указал в Microsoft Word для этого документа.

Этот объект никогда не бывает нулевым.

### Примеры

Показывает, как выполнить слияние почты с данными из объекта источника данных Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Создаем источник данных в виде ASCII-файла с символом "|" персонаж
// действует как разделитель, разделяющий столбцы. Первая строка содержит имена трех столбцов,
// и каждая последующая строка представляет собой строку с соответствующими значениями.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

// Открытие этого документа в Microsoft Word приведет к выполнению слияния перед отображением содержимого. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Смотрите также

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


