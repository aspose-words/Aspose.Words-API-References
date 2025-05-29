---
title: MailMerger Class
linktitle: MailMerger
articleTitle: MailMerger
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.LowCode.MailMerger. Легко заполняйте шаблоны данными, используя простые и продвинутые методы слияния почты для бесшовной автоматизации документов.
type: docs
weight: 4270
url: /ru/net/aspose.words.lowcode/mailmerger/
---
## MailMerger class

Предоставляет методы, предназначенные для заполнения шаблона данными с использованием простых операций слияния почты и слияния почты с областями.

```csharp
public class MailMerger : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/mailmerger/create/)(*[MailMergerContext](../mailmergercontext/)*) | Создает новый экземпляр процессора слияния почты. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_12)(*string, string, DataRow*) | Выполняет слияние почты из DataRow в документ. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_13)(*string, string, DataTable*) | Выполняет слияние почты из DataTable в документ. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_14)(*string, string, string[], object[]*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ и отображает результат в изображениях. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ и отображает результат в изображениях. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ и отображает результат в изображениях. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_4)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataRow в документ и отображает результат в изображениях. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_2)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи и отображает результат в виде изображений. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_5)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи и отображает результат в виде изображений. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_8)(*string, string, DataSet*) | Выполняет слияние почты из DataSet в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_9)(*string, string, DataTable*) | Выполняет слияние почты из DataTable в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataSet в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataSet в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет операцию слияния почты для одной записи. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataSet в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataTable в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataSet в документ с областями слияния почты. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataTable в документ с областями слияния почты. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataSet в документ с областями слияния почты и отображает результат в виде изображений. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataTable в документ с областями слияния почты и отображает результат в виде изображений. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataSet в документ с областями слияния почты и отображает результат в виде изображений. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Выполняет слияние почты из DataTable в документ с областями слияния почты и отображает результат в виде изображений. |

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
