---
title: "Aspose::Words::MailMerging::MailMerge class"
linktitle: "MailMerge"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MailMerge 类。表示邮件合并功能。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


表示邮件合并功能。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class MailMerge : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [DeleteFields](./deletefields/)() | 从文档中删除邮件合并相关字段。 |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | 从自定义数据源执行邮件合并。 |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | 对单条记录执行邮件合并操作。 |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | 从自定义数据源并使用邮件合并区域执行邮件合并。 |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | 从自定义数据源并使用邮件合并区域执行邮件合并。 |
| [get_CleanupOptions](./get_cleanupoptions/)() const | 获取一组标志，指定在邮件合并期间应删除哪些项目。 |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | 获取或设置一个值，指示带有标点符号的段落是否被视为空，并在指定了 [RemoveEmptyParagraphs](../mailmergecleanupoptions/) 选项时应被删除。 |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | 在文档中遇到邮件合并字段时，在邮件合并过程中发生。 |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | 允许在邮件合并期间处理特定事件。 |
| [get_MappedDataFields](./get_mappeddatafields/)() | 返回表示邮件合并操作映射数据字段的集合。 |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | 获取一个值，指示在针对数据源执行带区域的邮件合并时，文档中所有具有数据源名称的邮件合并区域是全部合并还是仅合并第一个。 |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | 获取一个值，指示在执行带区域的邮件合并时，是否更新整个文档中的字段。 |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | 获取一个值，指示是否应保留未使用的 \"mustache\" 标签。 |
| [get_RegionEndTag](./get_regionendtag/)() const | 获取邮件合并区域结束标签。 |
| [get_RegionStartTag](./get_regionstarttag/)() const | 获取邮件合并区域开始标签。 |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | 获取一个值，指示在执行邮件合并后，列表是否在每个节重新开始。 |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | 获取一个值，指示在邮件合并期间，第一文档节的 [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) 以及其在后续数据源行的副本是保持不变还是根据 MS Word 行为进行更新。 |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | 获取一个值，指示是否从邮件合并值中修剪前导和尾随空白。 |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | 获取一个值，指示合并字段和合并区域是否在不考虑父 IF 字段条件的情况下进行合并。 |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | 当 **true** 时，指定除了 MERGEFIELD 字段之外，邮件合并还会执行到其他类型的字段以及 \"{{fieldName}}\" 标签中。 |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | 获取一个值，指示是否应将包含 **TableStart** 或 **TableEnd** 字段的整段或 **TableStart** 与 **TableEnd** 字段之间的特定范围包含到邮件合并区域中。 |
| [GetFieldNames](./getfieldnames/)() | 返回文档中可用的邮件合并字段名称集合。 |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | 返回区域中可用的邮件合并字段名称集合。 |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | 返回区域中可用的邮件合并字段名称集合。 |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | 返回具有指定名称的邮件合并区域集合。 |
| [GetRegionsHierarchy](./getregionshierarchy/)() | 返回文档中可用的区域（含字段）的完整层次结构。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | 设置一组标志，指定在邮件合并期间应删除哪些项目。 |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | 用于设置 [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/) 的方法。 |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | 在文档中遇到邮件合并字段时，在邮件合并过程中发生。 |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | 允许在邮件合并期间处理特定事件。 |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | 设置一个值，指示在针对数据源执行带区域的邮件合并时，文档中所有具有数据源名称的邮件合并区域是全部合并还是仅合并第一个。 |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | 设置一个值，指示在执行带区域的邮件合并时，是否更新整个文档中的字段。 |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | 设置一个值，指示是否应保留未使用的 \"mustache\" 标签。 |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | 设置邮件合并区域结束标签。 |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | 设置邮件合并区域开始标签。 |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | 设置一个值，指示在执行邮件合并后，列表是否在每个节重新开始。 |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | 设置一个值，指示在邮件合并期间，第一文档节的 [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) 以及其在后续数据源行的副本是保持不变还是根据 MS Word 行为进行更新。 |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | 设置一个值，指示是否从邮件合并值中修剪前导和尾随空白。 |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | 设置一个值，指示是否在不考虑父 IF 字段条件的情况下合并合并字段和合并区域。 |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | 用于 [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/) 的设置器。 |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | 设置一个值，指示是否应将包含 **TableStart** 或 **TableEnd** 字段的整个段落或 **TableStart** 与 **TableEnd** 字段之间的特定范围包含到邮件合并区域中。 |
| static [Type](./type/)() |  |
## 备注


要使邮件合并操作生效，文档应包含 Word MERGEFIELD 字段，且可选地包含 NEXT 字段。在邮件合并过程中，文档中的合并字段会被来自数据源的值替换。

使用邮件合并有两种不同方式：使用邮件合并区域和不使用。

最简单的邮件合并是不使用区域，它与 Word 中的邮件合并工作方式非常相似。使用 **Execute** 方法将来自某些数据源（例如 **DataTable**、**DataSet** 或对象数组）的信息合并到文档中。[MailMerge](./) 对象会处理数据源的所有记录，并为每条记录复制并追加整个文档的内容。

请注意，当 [MailMerge](./) 对象遇到 NEXT 字段时，它会选择数据源中的下一条记录并继续合并，而不复制任何内容。

使用 [ExecuteWithRegions()](../) 及其他重载方法，将信息合并到已定义邮件合并区域的文档中。您可以将其用作此操作的数据源。

如果您希望在文档内部动态扩展部分内容，则需要使用邮件合并区域。若不使用邮件合并区域，整个文档将为数据源的每条记录重复一次。

## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
