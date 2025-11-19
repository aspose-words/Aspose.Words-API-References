---
title: MailMergerContext class
linktitle: MailMergerContext class
articleTitle: MailMergerContext class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.MailMergerContext class. Mail merge context."
type: docs
weight: 80
url: /python-net/aspose.words.lowcode/mailmergercontext/
---

## MailMergerContext class

Mail merge context.


**Inheritance:** [MailMergerContext](./) → [ProcessorContext](../processorcontext/)

### Constructors
| Name | Description |
| --- | --- |
| [MailMergerContext()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [font_settings](../processorcontext/font_settings/) | Font settings used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [layout_options](../processorcontext/layout_options/) | Document layout options used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [mail_merge_options](./mail_merge_options/) | Mail merge options. |
| [warning_callback](../processorcontext/warning_callback/) | Warning callback used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |

### Methods

| Name | Description |
| --- | --- |
|[ set_simple_data_source(field_names, field_values)](./set_simple_data_source/#strlist_objectlist) | Sets data source used to execute simple mail merge. |

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

* module [aspose.words.lowcode](../)
* class [ProcessorContext](../processorcontext/)

