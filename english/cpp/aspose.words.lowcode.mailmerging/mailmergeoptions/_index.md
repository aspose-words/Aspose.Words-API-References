---
title: Aspose::Words::LowCode::MailMerging::MailMergeOptions class
linktitle: MailMergeOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::MailMerging::MailMergeOptions class. Represents options for the mail merge functionality in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.lowcode.mailmerging/mailmergeoptions/
---
## MailMergeOptions class


Represents options for the mail merge functionality.

```cpp
class MailMergeOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Gets a set of flags that specify what items should be removed during mail merge. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) option is specified. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Gets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Gets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Gets a value indicating whether the unused "mustache" tags should be preserved. |
| [get_RegionEndTag](./get_regionendtag/)() const | Gets a mail merge region end tag. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Gets a mail merge region start tag. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Gets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Gets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Gets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Gets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | When **true**, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Gets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Sets a set of flags that specify what items should be removed during mail merge. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Setter for [Aspose::Words::LowCode::MailMerging::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Sets a value indicating whether the unused "mustache" tags should be preserved. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Sets a mail merge region end tag. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Sets a mail merge region start tag. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Sets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Setter for [Aspose::Words::LowCode::MailMerging::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::LowCode::MailMerging](../)
* Library [Aspose.Words for C++](../../)
