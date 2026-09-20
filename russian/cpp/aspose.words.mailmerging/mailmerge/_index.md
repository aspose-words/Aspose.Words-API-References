---
title: "Класс Aspose::Words::MailMerging::MailMerge"
linktitle: "MailMerge"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::MailMerging::MailMerge. Представляет функциональность слияния почты. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Представляет функциональность слияния почты. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [DeleteFields](./deletefields/)() | Удаляет из документа поля, связанные со слиянием почты. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Выполняет слияние почты из пользовательского источника данных. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Выполняет операцию слияния почты для одной записи. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Выполняет слияние почты из пользовательского источника данных с регионами слияния почты. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Выполняет слияние почты из пользовательского источника данных с регионами слияния почты. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Возвращает набор флагов, указывающих, какие элементы следует удалить во время слияния почты. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Получает или задает значение, указывающее, считаются ли абзацы с знаками пунктуации пустыми и должны ли они быть удалены, если указана опция [RemoveEmptyParagraphs](../mailmergecleanupoptions/). |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Происходит во время слияния почты, когда в документе встречается поле слияния почты. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Позволяет обрабатывать определённые события во время слияния почты. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Возвращает коллекцию, представляющую сопоставленные поля данных для операции слияния почты. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Получает значение, указывающее, должны ли все регионы слияния почты в документе с именем источника данных быть объединены при выполнении слияния почты с регионами против источника данных, или только первый. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Получает значение, указывающее, обновляются ли поля во всём документе при выполнении слияния почты с регионами. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Получает значение, указывающее, следует ли сохранять неиспользуемые теги "mustache". |
| [get_RegionEndTag](./get_regionendtag/)() const | Получает тег окончания региона слияния почты. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Получает тег начала региона слияния почты. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Получает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Получает значение, указывающее, сохраняются ли [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) первой секции документа и её копии для последующих строк источника данных во время слияния почты или обновляются в соответствии с поведением MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Получает значение, указывающее, обрезаются ли начальные и конечные пробелы в значениях слияния почты. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Получает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Когда **true**, указывает, что помимо полей MERGEFIELD слияние почты выполняется и в некоторые другие типы полей, а также в теги "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Получает значение, указывающее, следует ли включать в регион слияния почты весь абзац с полем **TableStart** или **TableEnd**, либо определённый диапазон между полями **TableStart** и **TableEnd**. |
| [GetFieldNames](./getfieldnames/)() | Возвращает коллекцию имён полей слияния почты, доступных в документе. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Возвращает коллекцию имён полей слияния почты, доступных в регионе. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Возвращает коллекцию имён полей слияния почты, доступных в регионе. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Возвращает коллекцию регионов слияния почты с указанным именем. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Возвращает полную иерархию регионов (с полями), доступных в документе. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Устанавливает набор флагов, определяющих, какие элементы следует удалять во время слияния почты. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Сеттер для [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Происходит во время слияния почты, когда в документе встречается поле слияния почты. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Позволяет обрабатывать определённые события во время слияния почты. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Устанавливает значение, указывающее, следует ли объединять все регионы слияния почты в документе с именем источника данных при выполнении слияния почты с регионами против источника данных или только первый. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Устанавливает значение, указывающее, обновляются ли поля во всём документе при выполнении слияния почты с регионами. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Устанавливает значение, указывающее, следует ли сохранять неиспользуемые теги "mustache". |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Устанавливает тег окончания региона слияния почты. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Устанавливает тег начала региона слияния почты. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Устанавливает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Устанавливает значение, указывающее, сохраняются ли [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) первой секции документа и её копии для последующих строк источника данных во время слияния почты или обновляются в соответствии с поведением MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Устанавливает значение, указывающее, обрезаются ли начальные и конечные пробелы в значениях слияния почты. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Устанавливает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Сеттер для [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Устанавливает значение, указывающее, следует ли включать в регион слияния почты весь абзац с полем **TableStart** или **TableEnd**, либо определённый диапазон между полями **TableStart** и **TableEnd**. |
| static [Type](./type/)() |  |
## Примечания


Чтобы операция слияния почты работала, документ должен содержать поля Word MERGEFIELD и, при необходимости, NEXT. Во время операции слияния почты поля слияния в документе заменяются значениями из вашего источника данных.

Существует два разных способа использования слияния почты: с регионами слияния почты и без них.

Самое простое слияние почты — без регионов, и оно очень похоже на то, как слияние почты работает в Word. Используйте методы **Execute** для слияния информации из какого-либо источника данных, такого как **DataTable**, **DataSet** или массив объектов, в ваш документ. Объект [MailMerge](./) обрабатывает все записи источника данных и копирует и добавляет содержимое всего документа для каждой записи.

Обратите внимание, что когда объект [MailMerge](./) встречает поле NEXT, он выбирает следующую запись в источнике данных и продолжает слияние без копирования какого-либо содержимого.

Используйте [ExecuteWithRegions()](../) и другие перегрузки для слияния информации в документ с определёнными регионами слияния почты. Вы можете использовать их в качестве источников данных для этой операции.

Вам необходимо использовать регионы слияния почты, если вы хотите динамически расширять части внутри документа. Без регионов слияния почты весь документ будет повторяться для каждой записи источника данных.

## См. также

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
