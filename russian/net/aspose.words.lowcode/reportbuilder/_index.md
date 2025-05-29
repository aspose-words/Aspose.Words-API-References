---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words для .NET
description: Создавайте динамические отчеты без усилий с помощью Aspose.Words LowCode ReportBuilder. Используйте LINQ Reporting Engine для беспрепятственного заполнения шаблонов данными.
type: docs
weight: 4360
url: /ru/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Предоставляет методы, предназначенные для заполнения шаблона данными с использованием LINQ Reporting Engine.

```csharp
public class ReportBuilder : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Создает новый экземпляр процессора построителя отчетов. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Создает новый экземпляр процессора построителя отчетов. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из входных и выходных потоков. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из входных и выходных потоков. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с именованной ссылкой на источник данных и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с дополнительными параметрами. Эта перегрузка автоматически определяет формат сохранения на основе расширения выходного файла. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, формируя завершенный отчет с указанным форматом вывода и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с именованной ссылкой на источник данных и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из указанных входных и выходных потоков файлов. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с именованной ссылкой на источник данных и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами из указанных входных и выходных потоков файлов. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с указанным форматом вывода, именованной ссылкой на источник данных и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из указанного источника, генерируя завершенный отчет с указанным форматом вывода, именованной ссылкой на источник данных и дополнительными параметрами. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников, генерируя завершенный отчет с указанным форматом вывода и дополнительными параметрами. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников. Преобразует вывод в изображения. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Заполняет шаблон документа данными из нескольких источников. Преобразует вывод в изображения. |

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
