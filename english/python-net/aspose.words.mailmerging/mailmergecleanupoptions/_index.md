---
title: MailMergeCleanupOptions enumeration
linktitle: MailMergeCleanupOptions enumeration
articleTitle: MailMergeCleanupOptions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.MailMergeCleanupOptions enumeration. Specifies options that determine what items are removed during mail merge."
type: docs
weight: 90
url: /python-net/aspose.words.mailmerging/mailmergecleanupoptions/
---

## MailMergeCleanupOptions enumeration

Specifies options that determine what items are removed during mail merge.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies a default value. |
| REMOVE_EMPTY_PARAGRAPHS | Specifies whether paragraphs that contained mail merge fields with no data should be removed from the document. When this option is set, paragraphs which contain region start and end merge fields which are otherwise empty are also removed. |
| REMOVE_UNUSED_REGIONS | Specifies whether unused mail merge regions should be removed from the document. |
| REMOVE_UNUSED_FIELDS | Specifies whether unused merge fields should be removed from the document. |
| REMOVE_CONTAINING_FIELDS | Specifies whether fields that contain merge fields (for example, IFs) should be removed from the document if the nested merge fields are removed. |
| REMOVE_STATIC_FIELDS | Specifies whether static fields should be removed from the document. Static fields are fields, which results remain the same upon any document change. Fields, which do not store their results in a document and are calculated on the fly (like [FieldType.FIELD_LIST_NUM](../../aspose.words.fields/fieldtype/#FIELD_LIST_NUM), [FieldType.FIELD_SYMBOL](../../aspose.words.fields/fieldtype/#FIELD_SYMBOL), etc.) are not considered to be static. |
| REMOVE_EMPTY_TABLE_ROWS | Specifies whether empty rows that contain mail merge regions should be removed from the document. |

### See Also

* module [aspose.words.mailmerging](../)

