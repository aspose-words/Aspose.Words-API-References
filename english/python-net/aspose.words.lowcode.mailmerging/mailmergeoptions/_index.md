---
title: MailMergeOptions class
linktitle: MailMergeOptions class
articleTitle: MailMergeOptions class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.mailmerging.MailMergeOptions class. Represents options for the mail merge functionality."
type: docs
weight: 10
url: /python-net/aspose.words.lowcode.mailmerging/mailmergeoptions/
---

## MailMergeOptions class

Represents options for the mail merge functionality.


### Constructors
| Name | Description |
| --- | --- |
| [MailMergeOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [cleanup_options](./cleanup_options/) | Gets or sets a set of flags that specify what items should be removed during mail merge. |
| [cleanup_paragraphs_with_punctuation_marks](./cleanup_paragraphs_with_punctuation_marks/) | Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS](../../aspose.words.mailmerging/mailmergecleanupoptions/#REMOVE_EMPTY_PARAGRAPHS) option is specified. |
| [merge_duplicate_regions](./merge_duplicate_regions/) | Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [merge_whole_document](./merge_whole_document/) | Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [preserve_unused_tags](./preserve_unused_tags/) | Gets or sets a value indicating whether the unused "mustache" tags should be preserved. |
| [region_end_tag](./region_end_tag/) | Gets or sets a mail merge region end tag. |
| [region_start_tag](./region_start_tag/) | Gets or sets a mail merge region start tag. |
| [restart_lists_at_each_section](./restart_lists_at_each_section/) | Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [retain_first_section_start](./retain_first_section_start/) | Gets or sets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [trim_whitespaces](./trim_whitespaces/) | Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [unconditional_merge_fields_and_regions](./unconditional_merge_fields_and_regions/) | Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [use_non_merge_fields](./use_non_merge_fields/) | When ``True``, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags. |
| [use_whole_paragraph_as_region](./use_whole_paragraph_as_region/) | Gets or sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |

### See Also

* module [aspose.words.lowcode.mailmerging](../)

