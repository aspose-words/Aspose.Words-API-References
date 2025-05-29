---
title: Comparer Class
linktitle: Comparer
articleTitle: Comparer
second_title: Aspose.Words для .NET
description: Легко сравнивайте документы с классом Aspose.Words LowCode Comparer. Откройте для себя мощные методы для бесшовного анализа документов и совместной работы.
type: docs
weight: 4210
url: /ru/net/aspose.words.lowcode/comparer/
---
## Comparer class

Предоставляет методы, предназначенные для сравнения документов.

```csharp
public class Comparer : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/comparer/create/#create)() | Создает новый экземпляр процессора преобразователя. |
| static [Create](../../aspose.words.lowcode/comparer/create/#create_1)(*[ComparerContext](../comparercontext/)*) | Создает новый экземпляр процессора сравнения. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_4)(*string, string, string, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанном выходном файле, создавая изменения в виде ряда редакций и редакций формата. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare)(*Stream, Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа, загруженных из потоков с дополнительными параметрами, и сохраняет различия в предоставленном выходном потоке в указанном формате сохранения, создавая изменения в виде ряда редакций и редакций формата. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_1)(*Stream, Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа, загруженных из потоков с дополнительными параметрами, и сохраняет различия в предоставленном выходном потоке в указанном формате сохранения, создавая изменения в виде ряда редакций и редакций формата. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_2)(*string, string, string, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанном выходном файле в предоставленном формате сохранения, создавая изменения в виде ряда редакций и редакций формата. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_3)(*string, string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанном выходном файле в предоставленном формате сохранения, создавая изменения в виде ряда редакций и редакций формата. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages)(*Stream, Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент в возвращаемом массиве представляет собой одну страницу вывода, представленную в виде изображения. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages_1)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент в возвращаемом массиве представляет собой одну страницу вывода, представленную в виде изображения. |

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
