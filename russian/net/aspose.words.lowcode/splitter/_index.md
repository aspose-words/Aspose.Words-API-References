---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words для .NET
description: Легко разделяйте документы с помощью класса Aspose.Words.LowCode.Splitter. Используйте универсальные методы для точного управления документами и повышения эффективности рабочего процесса.
type: docs
weight: 4420
url: /ru/net/aspose.words.lowcode/splitter/
---
## Splitter class

Предоставляет методы, предназначенные для разделения документов на части с использованием различных критериев.

```csharp
public class Splitter : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Создает новый экземпляр процессора-разделителя. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Извлекает указанный диапазон страниц из файла документа и сохраняет извлеченные страницы в новый файл. Формат выходного файла определяется расширением имени выходного файла. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Извлекает указанный диапазон страниц из потока документов и сохраняет извлеченные страницы в выходной поток, используя указанный формат сохранения. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Извлекает указанный диапазон страниц из потока документов и сохраняет извлеченные страницы в выходной поток, используя указанный формат сохранения. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Извлекает указанный диапазон страниц из файла документа и сохраняет извлеченные страницы в новый файл, используя указанный формат сохранения. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Извлекает указанный диапазон страниц из файла документа и сохраняет извлеченные страницы в новый файл, используя указанный формат сохранения. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Удаляет пустые страницы из документа и сохраняет вывод. Возвращает список номеров страниц, которые были удалены. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Удаляет пустые страницы из документа, предоставленного во входном потоке, и сохраняет обновленный документ в выходном потоке в указанном формате сохранения. Возвращает список номеров страниц, которые были удалены. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Удаляет пустые страницы из документа, предоставленного во входном потоке, и сохраняет обновленный документ в выходном потоке в указанном формате сохранения. Возвращает список номеров страниц, которые были удалены. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Удаляет пустые страницы из документа и сохраняет вывод в указанном формате. Возвращает список номеров страниц, которые были удалены. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Удаляет пустые страницы из документа и сохраняет вывод в указанном формате. Возвращает список номеров страниц, которые были удалены. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Разделяет документ из входного потока на несколько частей на основе указанных параметров разделения и возвращает полученные части в виде массива потоков в указанном формате сохранения. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Разделяет документ из входного потока на несколько частей на основе указанных параметров разделения и возвращает полученные части в виде массива потоков в указанном формате сохранения. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Разделяет документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы. Формат выходного файла определяется расширением имени выходного файла. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Разбивает документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы в указанном формате сохранения. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Разбивает документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы в указанном формате сохранения. |

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
