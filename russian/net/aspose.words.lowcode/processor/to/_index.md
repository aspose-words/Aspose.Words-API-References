---
title: Processor.To
linktitle: To
articleTitle: To
second_title: Aspose.Words для .NET
description: Оптимизируйте свой рабочий процесс с помощью нашего метода обработки, который четко определяет выходные файлы, повышая эффективность и оптимизируя задачи по управлению данными.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

Указывает выходной файл для процессора.

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| output | String | Имя выходного файла. |
| saveOptions | SaveOptions | Необязательные параметры сохранения. Если не указано, формат сохранения определяется расширением файла. |

### Возвращаемое значение

Возвращает процессор с указанным выходным файлом.

## Примечания

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла для каждой части в соответствии с правилом: 'outputFile_partIndex.extension'.

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

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

Указывает выходной файл для процессора.

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| output | String | Имя выходного файла. |
| saveFormat | SaveFormat | Формат сохранения. Если не указано, формат сохранения определяется расширением файла. |

### Возвращаемое значение

Возвращает процессор с указанным выходным файлом.

## Примечания

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла для каждой части в соответствии с правилом: 'outputFile_partIndex.extension'.

## Примеры

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

Указывает выходной поток для процессора.

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| output | Stream | Выходной поток. |
| saveOptions | SaveOptions | Сохранить параметры. |

### Возвращаемое значение

Возвращает процессор с указанным выходным потоком.

## Примечания

Если выходные данные состоят из нескольких файлов, в указанный поток будет сохранена только первая часть.

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

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

Указывает выходной поток для процессора.

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| output | Stream | Выходной поток. |
| saveFormat | SaveFormat | Сохранить формат. |

### Возвращаемое значение

Возвращает процессор с указанным выходным потоком.

## Примечания

Если выходные данные состоят из нескольких файлов, в указанный поток будет сохранена только первая часть.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

Указывает список выходных потоков документов.

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| output | List`1 | Список выходных потоков документов. |
| saveOptions | SaveOptions | Сохранить параметры. |

### Возвращаемое значение

Возвращает процессор с указанным списком выходных потоков документов.

## Примечания

Если вывод состоит из нескольких файлов (например, изображений или частей разделенного документа), поток для каждой части добавляется в указанный список. Если вывод представляет собой один файл, в список добавляется только один поток. Ответственность за утилизацию созданных потоков лежит на конечном пользователе.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

Указывает список выходных потоков документов.

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| output | List`1 | Список выходных потоков документов. |
| saveFormat | SaveFormat | Сохранить формат. |

### Возвращаемое значение

Возвращает процессор с указанным списком выходных потоков документов.

## Примечания

Если вывод состоит из нескольких файлов (например, изображений или частей разделенного документа), поток для каждой части добавляется в указанный список. Если вывод представляет собой один файл, в список добавляется только один поток. Ответственность за утилизацию созданных потоков лежит на конечном пользователе.

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
