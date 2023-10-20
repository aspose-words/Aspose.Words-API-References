---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: Aspose.Words для .NET
description: Aspose.Words.Settings.MailMergeMainDocumentType перечисление. Указывает возможные типы исходного документа слияния почты на С#.
type: docs
weight: 5840
url: /ru/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Указывает возможные типы исходного документа слияния почты.

```csharp
public enum MailMergeMainDocumentType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| NotAMergeDocument | `0` | Этот документ не является документом слияния почты. |
| FormLetters | `1` | Указывает, что исходный документ слияния почты имеет тип письма. |
| MailingLabels | `2` | Указывает, что исходный документ слияния почты имеет тип почтовой метки. |
| Envelopes | `4` | Указывает, что исходный документ слияния почты имеет тип конверта. |
| Catalog | `8` | Указывает, что исходный документ слияния почты имеет тип каталога. |
| Email | `16` | Указывает, что исходный документ слияния почты имеет тип сообщения электронной почты. |
| Fax | `32` | Указывает, что исходный документ слияния почты имеет тип факса. |
| Default | `0` | РавноNotAMergeDocument |

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

// Создаем источник данных в виде ASCII-файла с символом "|" характер
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

 // Открытие этого документа в Microsoft Word приведет к выполнению слияния почты перед отображением содержимого.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Смотрите также

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
