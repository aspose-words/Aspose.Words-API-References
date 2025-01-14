---
title: MailMergeOptions.trim_whitespaces property
linktitle: trim_whitespaces property
articleTitle: trim_whitespaces property
second_title: Aspose.Words for Python
description: "MailMergeOptions.trim_whitespaces property. Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values."
type: docs
weight: 110
url: /python-net/aspose.words.lowcode/mailmergeoptions/trim_whitespaces/
---

## MailMergeOptions.trim_whitespaces property

Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.


```python
@property
def trim_whitespaces(self) -> bool:
    ...

@trim_whitespaces.setter
def trim_whitespaces(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.



### Examples

Shows how to do mail merge operation for a single record.

```python
# There is a several ways to do mail merge operation:
doc = MY_DIR + 'Mail merge.doc'
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
aw.lowcode.MailMerger.execute(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.MailMerge.1.docx', field_names=field_names, field_values=field_values)
aw.lowcode.MailMerger.execute(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.MailMerge.2.docx', save_format=aw.SaveFormat.DOCX, field_names=field_names, field_values=field_values)
mail_merge_options = aw.lowcode.MailMergeOptions()
mail_merge_options.trim_whitespaces = True
aw.lowcode.MailMerger.execute(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.MailMerge.3.docx', save_format=aw.SaveFormat.DOCX, mail_merge_options=mail_merge_options, field_names=field_names, field_values=field_values)
```

### See Also

* module [aspose.words.lowcode](../../)
* class [MailMergeOptions](../)

