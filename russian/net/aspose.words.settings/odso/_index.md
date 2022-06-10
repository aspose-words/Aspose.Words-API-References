---
title: Odso
second_title: Справочник по API Aspose.Words для .NET
description: Указывает параметры объекта источника данных Office ODSO для источника данных слияния.
type: docs
weight: 5530
url: /ru/net/aspose.words.settings/odso/
---
## Odso class

Указывает параметры объекта источника данных Office (ODSO) для источника данных слияния.

```csharp
public class Odso
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Odso](odso)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter) { get; set; } | Указывает символ, который должен интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию равно 0, что означает отсутствие определенного разделителя столбцов. |
| [DataSource](../../aspose.words.settings/odso/datasource) { get; set; } | Указывает расположение внешнего источника данных, который необходимо подключить к документу для выполнения слияния. Значение по умолчанию — пустая строка. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype) { get; set; } | Указывает тип внешнего источника данных, к которому необходимо подключиться как часть информации о соединении ODSO для этого слияния. Значение по умолчанию:Default. |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas) { get; set; } | Получает или задает набор объектов, указывающих, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. Этот объект никогда не бывает нулевым. |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames) { get; set; } | Указывает, что хост-приложение должно обрабатывать первую строку данных в указанных внешних данных source как строку заголовка, содержащую имена каждого столбца. в источнике данных. Значение по умолчанию:` false` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas) { get; set; } | Получает или задает набор объектов, определяющих включение/исключение отдельных записей при слиянии. Этот объект никогда не бывает нулевым. |
| [TableName](../../aspose.words.settings/odso/tablename) { get; set; } | Указывает конкретный набор данных, к которому источник должен быть подключен во внешнем источнике данных. Значение по умолчанию — пустая строка. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring) { get; set; } | Указывает строку подключения к универсальному каналу передачи данных (UDL), используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone)() | Возвращает глубокий клон этого объекта. |

### Примечания

ODSO кажется «новым» способом, которым более новые версии Microsoft Word предпочитают использовать при указании определенные типы источников данных для документа слияния. ODSO, вероятно, впервые появился в Microsoft Word 2000.

Использование ODSO плохо документировано, и это лучший способ узнать, как использовать свойства этого объекта заключается в создании документа с нужным источником данных вручную в Microsoft Word, а затем открытии этого документа с помощью Aspose.Words и просмотре свойств файла[`MailMergeSettings`](../../aspose.words/document/mailmergesettings)и [`Odso`](../mailmergesettings/odso)объекты. Это хороший подход, если вы хотите узнать, как программно настроить источник данных, например.

Обычно вам не нужно создавать объекты этого класса напрямую, потому что настройки ODSO всегда доступны через[`Odso`](../mailmergesettings/odso)свойство.

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

 // Открытие этого документа в Microsoft Word приведет к выполнению слияния перед отображением содержимого. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
