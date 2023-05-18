---
title: Aspose::Words::MailMerging::MailMergeCleanupOptions enum
linktitle: MailMergeCleanupOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMergeCleanupOptions enum. Specifies options that determine what items are removed during mail merge in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Specifies options that determine what items are removed during mail merge.

```cpp
enum class MailMergeCleanupOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Specifies a default value. |
| RemoveEmptyParagraphs | 1 | Specifies whether paragraphs that contained mail merge fields with no data should be removed from the document. When this option is set, paragraphs which contain region start and end merge fields which are otherwise empty are also removed. |
| RemoveUnusedRegions | 2 | Specifies whether unused mail merge regions should be removed from the document. |
| RemoveUnusedFields | 4 | Specifies whether unused merge fields should be removed from the document. |
| RemoveContainingFields | 8 | Specifies whether fields that contain merge fields (for example, IFs) should be removed from the document if the nested merge fields are removed. |
| RemoveStaticFields | 16 | Specifies whether static fields should be removed from the document. Static fields are fields, which results remain the same upon any document change. [Fields](../../aspose.words.fields/), which do not store their results in a document and are calculated on the fly (like [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), etc.) are not considered to be static. |
| RemoveEmptyTableRows | 32 | Specifies whether empty rows that contain mail merge regions should be removed from the document. |

## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
