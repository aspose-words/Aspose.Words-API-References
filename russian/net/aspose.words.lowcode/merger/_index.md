---
title: Merger Class
linktitle: Merger
articleTitle: Merger
second_title: Aspose.Words для .NET
description: Легко объединяйте различные типы документов в один с классом Aspose.Words.LowCode.Merger. Оптимизируйте свой рабочий процесс и повысьте производительность уже сегодня!
type: docs
weight: 4300
url: /ru/net/aspose.words.lowcode/merger/
---
## Merger class

Представляет собой группу методов, предназначенных для объединения различных типов документов в один выходной документ.

```csharp
public class Merger : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/merger/create/#create)() | Создает новый экземпляр процессора слияния почты. |
| static [Create](../../aspose.words.lowcode/merger/create/#create_1)(*[MergerContext](../mergercontext/)*) | Создает новый экземпляр процессора слияния почты. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge)(*Document[], [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один документ и возвращает[`Document`](../../aspose.words/document/) экземпляр окончательного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_2)(*Stream[], [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один документ и возвращает[`Document`](../../aspose.words/document/) экземпляр окончательного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_8)(*string, string[]*) | Объединяет указанные входные документы в один выходной документ, используя указанные входные и имена выходных файлов, используяKeepSourceFormatting . |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_4)(*string[], [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один документ и возвращает[`Document`](../../aspose.words/document/) экземпляр окончательного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_6)(*Stream, Stream[], [SaveFormat](../../aspose.words/saveformat/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные входные/выходные потоки и формат конечного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_1)(*Stream[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один документ и возвращает[`Document`](../../aspose.words/document/) экземпляр окончательного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_3)(*string[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один документ и возвращает[`Document`](../../aspose.words/document/) экземпляр окончательного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_7)(*Stream, Stream[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные потоки ввода-вывода и параметры сохранения. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_10)(*string, string[], [SaveFormat](../../aspose.words/saveformat/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные имена входных/выходных файлов и формат конечного документа. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_11)(*string, string[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные имена входных и выходных файлов и параметры сохранения. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_5)(*Stream, Stream[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные потоки ввода-вывода и параметры сохранения. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_9)(*string, string[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные имена входных и выходных файлов и параметры сохранения. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages)(*Stream[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные потоки входных документов в один выходной документ, используя указанные параметры сохранения изображений. Преобразует выходные данные в изображения. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages_1)(*string[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Объединяет указанные входные документы в один выходной документ, используя указанные имена входных и выходных файлов и параметры сохранения. Преобразует выходные данные в изображения. |

## Примечания

Указанные входные и выходные файлы или потоки, а также требуемые параметры слияния и сохранения, используются для объединения указанных входных документов в один выходной документ.

Функция объединения поддерживает более 35 различных форматов файлов.

## Примеры

Показывает, как объединить документы в один выходной документ.

```csharp
//Существует несколько способов объединения документов:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
