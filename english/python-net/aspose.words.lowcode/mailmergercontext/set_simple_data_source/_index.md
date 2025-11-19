---
title: MailMergerContext.set_simple_data_source method
linktitle: set_simple_data_source method
articleTitle: set_simple_data_source method
second_title: Aspose.Words for Python
description: "MailMergerContext.set_simple_data_source method. Sets data source used to execute simple mail merge."
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/mailmergercontext/set_simple_data_source/
---

## set_simple_data_source(field_names, field_values) {#strlist_objectlist}

Sets data source used to execute simple mail merge.


```python
def set_simple_data_source(self, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_names | List[str] |  |
| field_values | List[object] |  |

### Remarks

If both simple mail merge data source and data source for mail merge with regions are specified,
mail merge with regions is executed first and then simple mail merge is executed.


### Examples

Shows how to do mail merge operation for a single record using context.

```python
# There is a several ways to do mail merge operation:
doc = MY_DIR + 'Mail merge.doc'
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
mail_merger_context = aw.lowcode.MailMergerContext()
mail_merger_context.set_simple_data_source(field_names=field_names, field_values=field_values)
mail_merger_context.mail_merge_options.trim_whitespaces = True
aw.lowcode.MailMerger.create(mail_merger_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.MailMergeContext.docx').execute()
```

Shows how to do mail merge operation for a single record from the stream using context.

```python
# There is a several ways to do mail merge operation using documents from the stream:
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
with system_helper.io.FileStream(MY_DIR + 'Mail merge.doc', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    mail_merger_context = aw.lowcode.MailMergerContext()
    mail_merger_context.set_simple_data_source(field_names=field_names, field_values=field_values)
    mail_merger_context.mail_merge_options.trim_whitespaces = True
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MailMergeContextStream.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.MailMerger.create(mail_merger_context).from_stream(input=stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../../)
* class [MailMergerContext](../)

