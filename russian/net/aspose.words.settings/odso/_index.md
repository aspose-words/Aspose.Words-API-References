---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Settings.Odso для бесшовной интеграции слияния почты. Оптимизируйте настройки ODSO для эффективного управления источниками данных.
type: docs
weight: 6710
url: /ru/net/aspose.words.settings/odso/
---
## Odso class

Указывает параметры объекта источника данных Office (ODSO) для источника данных слияния почты.

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public class Odso
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Odso](odso/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Указывает символ, который должен интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию — 0, что означает, что разделитель столбцов не определен. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Указывает местоположение внешнего источника данных, который будет подключен к документу для выполнения слияния почты. Значение по умолчанию — пустая строка. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Указывает тип внешнего источника данных, к которому будет осуществляться подключение в рамках информации о подключении ODSO для этого слияния почты. Значение по умолчанию:Default . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Возвращает или задает коллекцию объектов, которые определяют, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. Этот объект никогда не`нулевой` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Указывает, что приложение хостинга должно обрабатывать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена каждого столбца в источнике данных. Значение по умолчанию:`ЛОЖЬ` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Возвращает или задает коллекцию объектов, которые определяют включение/исключение отдельных записей в слияние. Этот объект никогда не`нулевой` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Указывает конкретный набор данных, к которому должен быть подключен источник во внешнем источнике данных. Значение по умолчанию — пустая строка. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Указывает строку подключения Universal Data Link (UDL), используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Возвращает глубокий клон этого объекта. |

## Примечания

ODSO, похоже, является "новым" способом, который более новые версии Microsoft Word предпочитают использовать при указании определенных типов источников данных для документа слияния. ODSO, вероятно, впервые появился в Microsoft Word 2000.

Использование ODSO плохо документировано, и лучший способ научиться использовать свойства этого объекта — это создать документ с нужным источником данных вручную в Microsoft Word, а затем открыть этот документ с помощью Aspose.Words и изучить свойства[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) и [`Odso`](../mailmergesettings/odso/)объекты. Это хороший подход, если вы хотите узнать, как программно настроить источник данных, например.

Обычно вам не нужно создавать объекты этого класса напрямую, поскольку настройки ODSO всегда доступны через[`Odso`](../mailmergesettings/odso/) свойство.

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
