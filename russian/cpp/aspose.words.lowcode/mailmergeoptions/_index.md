---
title: "Класс Aspose::Words::LowCode::MailMergeOptions"
linktitle: "MailMergeOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::LowCode::MailMergeOptions. Представляет параметры для функции слияния почты в C++."
type: docs
weight: 750
url: /ru/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Представляет параметры функции слияния почты.

```cpp
class MailMergeOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Возвращает набор флагов, указывающих, какие элементы следует удалить во время слияния почты. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Получает или задает значение, указывающее, считаются ли абзацы с знаками пунктуации пустыми и должны ли они быть удалены, если указана опция [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/). |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Получает значение, указывающее, должны ли все регионы слияния почты в документе с именем источника данных быть объединены при выполнении слияния почты с регионами против источника данных, или только первый. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Получает значение, указывающее, обновляются ли поля во всём документе при выполнении слияния почты с регионами. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Получает значение, указывающее, следует ли сохранять неиспользуемые теги "mustache". |
| [get_RegionEndTag](./get_regionendtag/)() const | Получает тег окончания региона слияния почты. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Получает тег начала региона слияния почты. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Получает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Получает значение, указывающее, сохраняется ли начало первого раздела документа и его копии для последующих строк источника данных во время слияния почты или обновляются в соответствии с поведением MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Получает значение, указывающее, обрезаются ли начальные и конечные пробелы в значениях слияния почты. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Получает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Когда **true**, указывает, что помимо полей MERGEFIELD слияние почты выполняется и в некоторые другие типы полей, а также в теги "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Получает значение, указывающее, следует ли включать в регион слияния почты весь абзац с полем **TableStart** или **TableEnd**, либо определённый диапазон между полями **TableStart** и **TableEnd**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Устанавливает набор флагов, определяющих, какие элементы следует удалять во время слияния почты. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Сеттер для [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Устанавливает значение, указывающее, следует ли объединять все регионы слияния почты в документе с именем источника данных при выполнении слияния почты с регионами против источника данных или только первый. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Устанавливает значение, указывающее, обновляются ли поля во всём документе при выполнении слияния почты с регионами. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Устанавливает значение, указывающее, следует ли сохранять неиспользуемые теги "mustache". |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Устанавливает тег окончания региона слияния почты. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Устанавливает тег начала региона слияния почты. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Устанавливает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Устанавливает значение, указывающее, сохраняется ли начало первого раздела документа и его копии для последующих строк источника данных во время слияния почты или обновляются в соответствии с поведением MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Устанавливает значение, указывающее, обрезаются ли начальные и конечные пробелы в значениях слияния почты. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Устанавливает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Сеттер для [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Устанавливает значение, указывающее, следует ли включать в регион слияния почты весь абзац с полем **TableStart** или **TableEnd**, либо определённый диапазон между полями **TableStart** и **TableEnd**. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
