---
title: ReportBuilder.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words для .NET
description: С легкостью создавайте индивидуальные отчеты с помощью метода BuildReport в ReportBuilder, заполняя шаблон данными для получения профессиональных результатов каждый раз.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/reportbuilder/buildreport/
---
## BuildReport(*string, string, object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_12}

Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| data | Object | Объект источника данных. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заполнить документ данными.

```csharp
public void BuildReportData()
{
    // Существует несколько способов заполнить документ данными:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Смотрите также

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_6}

Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| data | Object | Объект источника данных. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заполнить документ данными.

```csharp
public void BuildReportData()
{
    // Существует несколько способов заполнить документ данными:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_9}

Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| data | Object | Объект источника данных. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport}

Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из входных и выходных потоков.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| outputStream | Stream | Выходной файловый поток. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| data | Object | Объект источника данных. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как заполнить документ данными, используя документы из потока.

```csharp
// Существует несколько способов заполнить документ данными, используя документы из потока:
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_3}

Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из входных и выходных потоков.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| outputStream | Stream | Выходной файловый поток. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| data | Object | Объект источника данных. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_13}

Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с именованной ссылкой на источник данных и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| data | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заполнить документ источниками данных.

```csharp
public void BuildReportDataSource()
{
    // Существует несколько способов заполнить документ источниками данных:
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Смотрите также

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_7}

Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с указанным форматом вывода, именованной ссылкой на источник данных и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| data | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заполнить документ источниками данных.

```csharp
public void BuildReportDataSource()
{
    // Существует несколько способов заполнить документ источниками данных:
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_10}

Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с указанным форматом вывода, именованной ссылкой на источник данных и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, string dataSourceName, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| data | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_1}

Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с именованной ссылкой на источник данных и дополнительными параметрами.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| outputStream | Stream | Выходной файловый поток. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| data | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как заполнить документ источниками данных, используя документы из потока.

```csharp
// Существует несколько способов заполнить документ источниками данных, используя документы из потока:
MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

using (FileStream streamIn = new FileStream(MyDir + "Report building.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" });

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.4.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.Create(reportBuilderContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_4}

Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с именованной ссылкой на источник данных и дополнительными параметрами.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| outputStream | Stream | Выходной файловый поток. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| data | Object | Объект источника данных. |
| dataSourceName | String | Имя для ссылки на объект источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_14}

Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с дополнительными параметрами. Эта перегрузка автоматически определяет формат сохранения на основе расширения выходного файла.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object[] data, 
    string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| data | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заполнить документ источниками данных.

```csharp
public void BuildReportDataSource()
{
    // Существует несколько способов заполнить документ источниками данных:
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Смотрите также

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_8}

Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| data | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

## Примеры

Показывает, как заполнить документ источниками данных.

```csharp
public void BuildReportDataSource()
{
    // Существует несколько способов заполнить документ источниками данных:
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_11}

Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object[] data, string[] dataSourceNames, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| data | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница выходных данных будет сохранена как отдельный файл. Указанное имя выходного файла будет использоваться для генерации имен файлов для каждой части в соответствии с правилом: outputFile_partIndex.extension.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый файл TIFF.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_2}

Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из указанных входных и выходных потоков файлов.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| outputStream | Stream | Выходной файловый поток. |
| saveFormat | SaveFormat | Формат сохранения выходных данных. |
| data | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

## Примеры

Показывает, как заполнить документ данными, используя документы из потока.

```csharp
// Существует несколько способов заполнить документ данными, используя документы из потока:
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_5}

Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из указанных входных и выходных потоков файлов.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| outputStream | Stream | Выходной файловый поток. |
| saveOptions | SaveOptions | Параметры сохранения выходных данных. |
| data | Object[] | Массив объектов источника данных. |
| dataSourceNames | String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |
| reportBuilderOptions | ReportBuilderOptions | Дополнительные параметры построения отчетов. |

## Примечания

Если выходной формат представляет собой изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), в указанном потоке будет сохранена только первая страница вывода.

Если выходной формат — TIFF, вывод будет сохранен как один многокадровый TIFF в указанном потоке.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
