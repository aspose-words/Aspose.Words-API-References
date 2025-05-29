---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.MailMergeOptions для бесшовных решений слияния почты с низким кодом. Улучшите автоматизацию документов с помощью настраиваемых функций!
type: docs
weight: 4260
url: /ru/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Представляет параметры для функции слияния почты.

```csharp
public class MailMergeOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Возвращает или задает набор флагов, которые определяют, какие элементы следует удалить во время слияния почты. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Возвращает или задает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, еслиRemoveEmptyParagraphs опция указана. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Возвращает или задает значение, указывающее, следует ли объединять все регионы слияния почты документа с именем источника данных при выполнении слияния почты с регионами по отношению к источнику данных или только первый из них. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Возвращает или задает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с регионами. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Возвращает или задает значение, указывающее, следует ли сохранять неиспользуемые теги «усы». |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Получает или задает конечный тег области слияния почты. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Получает или задает начальный тег области слияния почты. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Возвращает или задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Возвращает или задает значение, указывающее, сохраняются ли начало раздела первого раздела документа и его копии для последующих строк источника данных rows во время слияния почты или обновляются в соответствии с поведением MS Word. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Возвращает или задает значение, указывающее, удаляются ли конечные и начальные пробелы из значений слияния почты. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Возвращает или задает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | Когда`истинный` , указывает, что в дополнение к полям MERGEFIELD слияние выполняется в некоторые другие типы полей и также в теги "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Возвращает или задает значение, указывающее, является ли весь абзац**TableStart** или**TableEnd** field или определенный диапазон между**TableStart** и**TableEnd** поля должны быть включены в область слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты для одной записи.

```csharp
// Существует несколько способов выполнить операцию слияния почты:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
