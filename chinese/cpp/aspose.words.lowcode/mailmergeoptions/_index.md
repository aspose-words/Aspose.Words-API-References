---
title: "Aspose::Words::LowCode::MailMergeOptions 类"
linktitle: "MailMergeOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::MailMergeOptions 类。表示 C++ 中邮件合并功能的选项。"
type: docs
weight: 750
url: /zh/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


表示邮件合并功能的选项。

```cpp
class MailMergeOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | 获取一组标志，指定在邮件合并期间应删除哪些项目。 |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | 获取或设置一个值，指示带有标点符号的段落是否被视为空，并在指定了 [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) 选项时应将其删除。 |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | 获取一个值，指示在针对数据源执行带区域的邮件合并时，文档中所有具有数据源名称的邮件合并区域是全部合并还是仅合并第一个。 |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | 获取一个值，指示在执行带区域的邮件合并时，是否更新整个文档中的字段。 |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | 获取一个值，指示是否应保留未使用的 \"mustache\" 标签。 |
| [get_RegionEndTag](./get_regionendtag/)() const | 获取邮件合并区域结束标签。 |
| [get_RegionStartTag](./get_regionstarttag/)() const | 获取邮件合并区域开始标签。 |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | 获取一个值，指示在执行邮件合并后，列表是否在每个节重新开始。 |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | 获取一个值，指示在邮件合并期间，是否保留第一文档节的节起始及其后续数据源行的副本，或根据 MS Word 行为进行更新。 |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | 获取一个值，指示是否从邮件合并值中修剪前导和尾随空白。 |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | 获取一个值，指示合并字段和合并区域是否在不考虑父 IF 字段条件的情况下进行合并。 |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | 当 **true** 时，指定除了 MERGEFIELD 字段之外，邮件合并还会执行到其他类型的字段以及 \"{{fieldName}}\" 标签中。 |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | 获取一个值，指示是否应将包含 **TableStart** 或 **TableEnd** 字段的整段或 **TableStart** 与 **TableEnd** 字段之间的特定范围包含到邮件合并区域中。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | 设置一组标志，指定在邮件合并期间应删除哪些项目。 |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | 用于设置 [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/) 的 setter。 |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | 设置一个值，指示在针对数据源执行带区域的邮件合并时，文档中所有具有数据源名称的邮件合并区域是全部合并还是仅合并第一个。 |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | 设置一个值，指示在执行带区域的邮件合并时，是否更新整个文档中的字段。 |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | 设置一个值，指示是否应保留未使用的 \"mustache\" 标签。 |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | 设置邮件合并区域结束标签。 |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | 设置邮件合并区域开始标签。 |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | 设置一个值，指示在执行邮件合并后，列表是否在每个节重新开始。 |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | 设置一个值，指示在邮件合并期间，是否保留第一文档节的节起始及其在后续数据源行的副本，或根据 MS Word 行为进行更新。 |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | 设置一个值，指示是否从邮件合并值中修剪前导和尾随空白。 |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | 设置一个值，指示是否在不考虑父 IF 字段条件的情况下合并合并字段和合并区域。 |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | 用于 [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/) 的设置器。 |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | 设置一个值，指示是否应将包含 **TableStart** 或 **TableEnd** 字段的整个段落或 **TableStart** 与 **TableEnd** 字段之间的特定范围包含到邮件合并区域中。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
