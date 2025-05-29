---
title: Replacer Class
linktitle: Replacer
articleTitle: Replacer
second_title: Aspose.Words для .NET
description: Легко заменяйте текст в документах с помощью Aspose.Words.LowCode.Replacer. Упростите свой рабочий процесс и улучшите управление документами уже сегодня!
type: docs
weight: 4340
url: /ru/net/aspose.words.lowcode/replacer/
---
## Replacer class

Предоставляет методы, предназначенные для поиска и замены текста в документе.

```csharp
public class Replacer : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/replacer/create/)(*[ReplacerContext](../replacercontext/)*) | Создает новый экземпляр процессора-заменителя. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_9)(*string, string, Regex, string*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле с использованием регулярного выражения. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_8)(*string, string, string, string*) | Заменяет все вхождения указанного шаблона строки символов на заменяющую строку во входном файле. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на заменяющую строку во входном потоке с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на заменяющую строку во входном потоке с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов заменяющей строкой во входном файле с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](../../aspose.words.lowcode/replacer/replace/#replace_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов заменяющей строкой во входном файле с указанным форматом сохранения и дополнительными параметрами. |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона регулярного выражения на строку замены во входном файле. Преобразует вывод в изображения. |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле. Преобразует вывод в изображения. |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона регулярного выражения на строку замены во входном файле. Преобразует вывод в изображения. |
| static [ReplaceToImages](../../aspose.words.lowcode/replacer/replacetoimages/#replacetoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на строку замены во входном файле. Преобразует вывод в изображения. |

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
