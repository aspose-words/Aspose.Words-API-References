---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words для .NET
description: Легко разделяйте документы на несколько разделов с помощью нашего гибкого метода Splitter Split. Сохраняйте в предпочитаемом вами формате для простого управления файлами!
type: docs
weight: 40
url: /ru/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Разделяет документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы. Формат выходного файла определяется расширением имени выходного файла.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла, используемое для генерации имени файла для частей документа с использованием правила «outputFile_partIndex.extension» |
| options | SplitOptions | Варианты разделения документа. |

## Примеры

Показывает, как разделить документ по страницам.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Смотрите также

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Разбивает документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы в указанном формате сохранения.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла, используемое для генерации имени файла для частей документа с использованием правила «outputFile_partIndex.extension» |
| saveFormat | SaveFormat | Формат сохранения. |
| options | SplitOptions | Варианты разделения документа. |

## Примеры

Показывает, как разделить документ по страницам.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Разбивает документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы в указанном формате сохранения.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| outputFileName | String | Имя выходного файла, используемое для генерации имени файла для частей документа с использованием правила «outputFile_partIndex.extension» |
| saveOptions | SaveOptions | Параметры сохранения. |
| options | SplitOptions | Варианты разделения документа. |

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Разделяет документ из входного потока на несколько частей на основе указанных параметров разделения и возвращает полученные части в виде массива потоков в указанном формате сохранения.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| saveFormat | SaveFormat | Формат сохранения. |
| options | SplitOptions | Варианты разделения документа. |

## Примеры

Показывает, как разделить документ из потока по страницам.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Разделяет документ из входного потока на несколько частей на основе указанных параметров разделения и возвращает полученные части в виде массива потоков в указанном формате сохранения.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |
| options | SplitOptions | Варианты разделения документа. |

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
