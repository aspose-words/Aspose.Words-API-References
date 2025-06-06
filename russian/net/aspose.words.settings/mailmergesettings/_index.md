---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.MailMergeSettings, чтобы оптимизировать автоматизацию документооборота с помощью мощных возможностей слияния почты для повышения эффективности.
type: docs
weight: 6680
url: /ru/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Указывает всю информацию о слиянии почты для документа.

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public class MailMergeSettings
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Указывает индекс записи из источника данных, который будет отображаться в Microsoft Word. Значение по умолчанию — 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Указывает столбец в источнике данных, содержащий адреса электронной почты. Значение по умолчанию — пустая строка. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Указывает тип отчета об ошибках, который будет создаваться Microsoft Word при выполнении слияния почты. Значение по умолчанию:Default . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Указывает строку подключения, используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Указывает путь к источнику данных для слияния почты. Значение по умолчанию — пустая строка. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Указывает тип источника данных для слияния почты и метод доступа к данным. Значение по умолчанию:Default . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Указывает, как Microsoft Word будет выводить результаты слияния почты. Значение по умолчанию:Default . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединенных документах, полученных в результате слияния почты. Значение по умолчанию:`ЛОЖЬ` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Указывает путь к источнику заголовка слияния почты. Значение по умолчанию — пустая строка. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Не уверен насчет этого. Справочник по автоматизации Microsoft Word предполагает, что это указывает на то, что запрос выполняется каждый раз, когда документ открывается в Microsoft Word. Но спецификация OOXML предполагает, что это указывает на то, что запрос содержит ссылку на внешний файл запроса, который содержит фактический запрос. Значение по умолчанию:`ЛОЖЬ` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Указывает, что документы, созданные во время операции слияния почты, должны быть отправлены по электронной почте как вложение, а не как тело самого письма. Значение по умолчанию:`ЛОЖЬ` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Указывает текст, который будет отображаться в строке темы электронных писем или факсов, создаваемых во время слияния почты. Значение по умолчанию — пустая строка. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Указывает основной тип документа для слияния почты. Значение по умолчанию:Default . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Возвращает или задает объект, который определяет параметры объекта источника данных Office (ODSO). |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Содержит строку языка структурированных запросов, которая должна быть запущена для указанного внешнего источника данных, чтобы вернуть набор записей, которые должны быть импортированы в документ при выполнении операции слияния почты. Значением по умолчанию является пустая строка. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных, в который были вставлены поля слияния (например, предварительный просмотр объединенных данных). Значение по умолчанию:`ЛОЖЬ` . |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Очищает настройки слияния почты таким образом, что при сохранении документа настройки слияния почты не сохраняются и он становится обычным документом. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Возвращает глубокий клон этого объекта. |

## Примечания

Вы можете использовать этот объект для указания источника данных слияния почты для документа, и эта информация (вместе с доступными полями данных) появится в Microsoft Word, когда пользователь откроет этот документ. Или вы можете использовать этот объект для запроса настроек слияния почты, которые пользователь указал в Microsoft Word для этого документа.

Обычно вам не нужно создавать объекты этого класса напрямую, поскольку настройки слияния документа всегда доступны через[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) свойство.

Чтобы определить, является ли этот документ основным документом слияния, проверьте значение [`MainDocumentType`](./maindocumenttype/) свойство.

Чтобы удалить настройки слияния почты и информацию об источнике данных из документа, можно использовать [`Clear`](./clear/) Метод. Aspose.Words не будет записывать настройки слияния в документ, если [`MainDocumentType`](./maindocumenttype/) свойство установлено наNotAMergeDocument или[`DataType`](./datatype/) свойство установлено наNone.

Лучший способ узнать, как использовать свойства этого объекта, — создать документ с нужным источником данных вручную в Microsoft Word, а затем открыть этот документ с помощью Aspose.Words и изучить свойства [`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) и[`Odso`](./odso/) объекты. Это хороший подход, если вы хотите узнать, как программно настроить источник данных, например.

Aspose.Words сохраняет информацию о слиянии почты при загрузке, сохранении и конвертации документов между различными форматами, но не использует эту информацию при выполнении собственного слияния почты с помощью[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) объект.

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
