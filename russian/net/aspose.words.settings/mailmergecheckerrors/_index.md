---
title: Enum MailMergeCheckErrors
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Settings.MailMergeCheckErrors перечисление. Указывает как Microsoft Word будет сообщать об ошибках обнаруженных во время слияния.
type: docs
weight: 5510
url: /ru/net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

Указывает, как Microsoft Word будет сообщать об ошибках, обнаруженных во время слияния.

```csharp
public enum MailMergeCheckErrors
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Simulate | `1` | Имитация слияния и сообщения об ошибках в новом документе. |
| PauseOnError | `2` | Завершите слияние и сделайте паузу, чтобы сообщить об ошибках. |
| CollectErrors | `3` | Завершите слияние и сообщите об ошибках в новом документе. |
| Default | `2` | равноPauseOnError значение. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)


