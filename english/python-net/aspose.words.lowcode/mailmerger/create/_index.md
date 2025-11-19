---
title: MailMerger.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "MailMerger.create method. Creates new instance of the mail merger processor."
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/mailmerger/create/
---

## create(context) {#mailmergercontext}

Creates new instance of the mail merger processor.


```python
def create(self, context: aspose.words.lowcode.MailMergerContext):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| context | [MailMergerContext](../../mailmergercontext/) |  |

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
* class [MailMerger](../)

