---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.MailMergeDestination, определяющее результаты для бесшовных слияний документов. Оптимизируйте обработку документов сегодня!
type: docs
weight: 6660
url: /ru/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Указывает возможные результаты, которые могут быть получены при выполнении слияния почты в документе.

```csharp
public enum MailMergeDestination
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| NewDocument | `0` | Указывает, что соответствующие приложения хостинга должны генерировать новые документы путем заполнения полей в заданном документе данными из указанного внешнего источника данных. |
| Printer | `1` | Указывает, что соответствующие приложения хостинга должны печатать документы, полученные в результате заполнения полей в заданном документе внешними данными из указанного внешнего источника данных. |
| Email | `2` | Указывает, что соответствующие приложения хостинга должны генерировать электронные письма с использованием документов, полученных в результате заполнения полей в указанном документе данными из указанного внешнего источника данных. |
| Fax | `4` | Указывает, что соответствующие приложения хостинга должны генерировать факсы с использованием документов, полученных в результате заполнения полей в указанном документе данными из указанного внешнего источника данных. |
| Default | `0` | РавноNewDocument значение. |

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

* property [Destination](../mailmergesettings/destination/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
