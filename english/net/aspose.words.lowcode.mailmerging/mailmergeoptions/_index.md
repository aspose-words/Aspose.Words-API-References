---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.MailMerging.MailMergeOptions class. Represents options for the mail merge functionality in C#.
type: docs
weight: 4200
url: /net/aspose.words.lowcode.mailmerging/mailmergeoptions/
---
## MailMergeOptions class

Represents options for the mail merge functionality.

```csharp
public class MailMergeOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode.mailmerging/mailmergeoptions/cleanupoptions/) { get; set; } | Gets or sets a set of flags that specify what items should be removed during mail merge. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode.mailmerging/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the RemoveEmptyParagraphs option is specified. |
| [MergeDuplicateRegions](../../aspose.words.lowcode.mailmerging/mailmergeoptions/mergeduplicateregions/) { get; set; } | Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [MergeWholeDocument](../../aspose.words.lowcode.mailmerging/mailmergeoptions/mergewholedocument/) { get; set; } | Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [PreserveUnusedTags](../../aspose.words.lowcode.mailmerging/mailmergeoptions/preserveunusedtags/) { get; set; } | Gets or sets a value indicating whether the unused "mustache" tags should be preserved. |
| [RegionEndTag](../../aspose.words.lowcode.mailmerging/mailmergeoptions/regionendtag/) { get; set; } | Gets or sets a mail merge region end tag. |
| [RegionStartTag](../../aspose.words.lowcode.mailmerging/mailmergeoptions/regionstarttag/) { get; set; } | Gets or sets a mail merge region start tag. |
| [RestartListsAtEachSection](../../aspose.words.lowcode.mailmerging/mailmergeoptions/restartlistsateachsection/) { get; set; } | Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [RetainFirstSectionStart](../../aspose.words.lowcode.mailmerging/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Gets or sets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [TrimWhitespaces](../../aspose.words.lowcode.mailmerging/mailmergeoptions/trimwhitespaces/) { get; set; } | Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode.mailmerging/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [UseNonMergeFields](../../aspose.words.lowcode.mailmerging/mailmergeoptions/usenonmergefields/) { get; set; } | When `true`, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags. |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode.mailmerging/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Gets or sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |

### See Also

* namespace [Aspose.Words.LowCode.MailMerging](../../aspose.words.lowcode.mailmerging/)
* assembly [Aspose.Words](../../)
