---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words OdsoDataSourceType, которое позволяет легко подключаться к внешним источникам данных и расширять возможности обработки документов.
type: docs
weight: 6720
url: /ru/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Указывает тип внешнего источника данных, к которому будет осуществляться подключение, как часть информации о подключении ODSO.

```csharp
public enum OdsoDataSourceType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Text | `0` | Указывает, что данный документ был подключен к текстовому файлу. Возможно wdMergeSubTypeOther. |
| Database | `1` | Указывает, что данный документ подключен к базе данных. Возможно wdMergeSubTypeAccess. |
| AddressBook | `2` | Указывает, что данный документ был подключен к адресной книге контактов. Возможно wdMergeSubTypeOAL. |
| Document1 | `3` | Указывает, что данный документ был подключен к другому формату документа, поддерживаемому создающим приложением. Возможно wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Указывает, что данный документ был связан с другим форматом документа, поддерживаемым создающим приложением. Возможно, wdMergeSubTypeWorks. |
| Native | `5` | Указывает, что данный документ был связан с другим форматом документа, являющимся собственным для создающего приложения. Возможно wdMergeSubTypeOLEDBText |
| Email | `6` | Указывает, что данный документ был подключен к приложению электронной почты. Возможно wdMergeSubTypeOutlook. |
| None | `7` | Тип внешнего источника данных не указан. Возможно wdMergeSubTypeWord. |
| Legacy | `8` | Указывает, что данный документ был подключен к устаревшему формату документа, поддерживаемому производящим приложением Возможно wdMergeSubTypeWord2000. |
| Master | `9` | Указывает, что данный документ подключен к источнику данных, который объединяет другие источники данных. |
| Default | `7` | РавноNone . |

## Примечания

Спецификация OOXML для этого перечисления очень расплывчата. Я предполагаю, что оно может соответствовать перечислению WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.

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

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
