---
title: Processor.From
linktitle: From
articleTitle: From
second_title: Aspose.Words для .NET
description: Улучшите свой рабочий процесс с помощью нашего процессора, который эффективно обрабатывает входящие документы, обеспечивая бесперебойную обработку и повышенную производительность.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/processor/from/
---
## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

Указывает входной документ для обработки.

```csharp
public Processor From(string input, LoadOptions loadOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| input | String | Введите имя файла документа. |
| loadOptions | LoadOptions | Дополнительные параметры загрузки, используемые для загрузки документа. |

### Возвращаемое значение

Возвращает процессор с указанным входным файлом.

## Примечания

Если процессор принимает только один файл в качестве входных данных, будет обработан только последний указанный файл. [`Merger`](../../merger/) процессор принимает на вход несколько файлов, в результате все указанные документы будут объединены. [`Converter`](../../converter/) Процессор принимает только один файл в качестве входных данных, поэтому будет преобразован только последний указанный файл.

## Примеры

Показывает, как преобразовывать документы с помощью одной строки кода, используя контекст.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Показывает, как объединить документы в один выходной документ с использованием контекста.

```csharp
//Существует несколько способов объединения документов:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from}

Указывает входной документ для обработки.

```csharp
public Processor From(Stream input, LoadOptions loadOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| input | Stream | Входной поток документов. |
| loadOptions | LoadOptions | Дополнительные параметры загрузки, используемые для загрузки документа. |

### Возвращаемое значение

Возвращает процессор с указанным потоком входного файла.

## Примечания

Если процессор принимает только один файл в качестве входных данных, будет обработан только последний указанный файл. [`Merger`](../../merger/) процессор принимает на вход несколько файлов, в результате все указанные документы будут объединены. [`Converter`](../../converter/) Процессор принимает только один файл в качестве входных данных, поэтому будет преобразован только последний указанный файл.

## Примеры

Показывает, как преобразовать документы из потока с помощью одной строки кода, используя контекст.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Показывает, как объединить документы из потока в один выходной документ с использованием контекста.

```csharp
//Существует несколько способов объединения документов:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
