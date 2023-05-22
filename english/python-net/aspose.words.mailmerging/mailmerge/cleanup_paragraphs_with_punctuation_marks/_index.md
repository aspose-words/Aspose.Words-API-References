---
title: MailMerge.cleanup_paragraphs_with_punctuation_marks property
linktitle: cleanup_paragraphs_with_punctuation_marks property
articleTitle: cleanup_paragraphs_with_punctuation_marks property
second_title: Aspose.Words for Python
description: "MailMerge.cleanup_paragraphs_with_punctuation_marks property. Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS](../../mailmergecleanupoptions/#REMOVE_EMPTY_PARAGRAPHS) option is specified."
type: docs
weight: 20
url: /python-net/aspose.words.mailmerging/mailmerge/cleanup_paragraphs_with_punctuation_marks/
---

## MailMerge.cleanup_paragraphs_with_punctuation_marks property

Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty
and should be removed if the [MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS](../../mailmergecleanupoptions/#REMOVE_EMPTY_PARAGRAPHS) option is specified.


The default value is ``True``.


Here is the complete list of cleanable punctuation marks:

* !
  
* ,
  
* .
  
* :
  
* ;
  
* ?
  
* ¡
  
* ¿
  



### Examples

Shows how to remove paragraphs with punctuation marks after a mail merge operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

merge_field_option1 = builder.insert_field("MERGEFIELD", "Option_1").as_field_merge_field()
merge_field_option1.field_name = "Option_1"

builder.write(punctuation_mark)

merge_field_option2 = builder.insert_field("MERGEFIELD", "Option_2").as_field_merge_field()
merge_field_option2.field_name = "Option_2"

# Configure the "cleanup_options" property to remove any empty paragraphs that this mail merge would create.
doc.mail_merge.cleanup_options = aw.mailmerging.MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS

# Setting the "cleanup_paragraphs_with_punctuation_marks" property to "True" will also count paragraphs
# with punctuation marks as empty and will get the mail merge operation to remove them as well.
# Setting the "cleanup_paragraphs_with_punctuation_marks" property to "False"
# will remove empty paragraphs, but not ones with punctuation marks.
# This is a list of punctuation marks that this property concerns: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.mail_merge.cleanup_paragraphs_with_punctuation_marks = cleanup_paragraphs_with_punctuation_marks

doc.mail_merge.execute(["Option_1", "Option_2"], [None, None])

doc.save(ARTIFACTS_DIR + "MailMerge.remove_colon_between_empty_merge_fields.docx")
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

