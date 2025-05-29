---
title: MailMergeSettings.CheckErrors
linktitle: CheckErrors
articleTitle: CheckErrors
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MailMergeSettings CheckErrors в Microsoft Word для эффективного сообщения об ошибках во время слияний почты. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.settings/mailmergesettings/checkerrors/
---
## MailMergeSettings.CheckErrors property

Указывает тип отчета об ошибках, который будет создаваться Microsoft Word при выполнении слияния почты. Значение по умолчанию:Default .

```csharp
public MailMergeCheckErrors CheckErrors { get; set; }
```

## Примеры

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

// Создаем источник данных в виде ASCII-файла с символом "|"
// действует как разделитель, который разделяет столбцы. Первая строка содержит имена трех столбцов,
// и каждая последующая строка — это строка с соответствующими им значениями.
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

 // При открытии этого документа в Microsoft Word будет выполнено слияние почты перед отображением содержимого.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Смотрите также

* enum [MailMergeCheckErrors](../../mailmergecheckerrors/)
* class [MailMergeSettings](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
