---
title: ComparerContext class
linktitle: ComparerContext class
articleTitle: ComparerContext class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.ComparerContext class. Document comparer context"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/comparercontext/
---

## ComparerContext class

Document comparer context


**Inheritance:** [ComparerContext](./) → [ProcessorContext](../processorcontext/)

### Constructors
| Name | Description |
| --- | --- |
| [ComparerContext()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [accept_revisions](./accept_revisions/) | Indicates whether to accept revisions in the documents before comparing them. If the compared documents contain revisions and this flag is set to false, the processor will reject revisions. Default is ``True``. |
| [author](./author/) | The author to be assigned to revisions created during document comparison. |
| [compare_options](./compare_options/) | Options used upon comparing documents. |
| [date_time](./date_time/) | The date and time assigned to revisions created during document comparison. |
| [font_settings](../processorcontext/font_settings/) | Font settings used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [layout_options](../processorcontext/layout_options/) | Document layout options used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [warning_callback](../processorcontext/warning_callback/) | Warning callback used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |

### Examples

Shows how to simple compare documents using context.

```python
# There is a several ways to compare documents:
first_doc = MY_DIR + 'Table column bookmarks.docx'
second_doc = MY_DIR + 'Table column bookmarks.doc'
comparer_context = aw.lowcode.ComparerContext()
comparer_context.compare_options.ignore_case_changes = True
comparer_context.author = 'Author'
comparer_context.date_time = datetime.datetime(1, 1, 1)
aw.lowcode.Comparer.create(comparer_context).from_file(input=first_doc).from_file(input=second_doc).to_file(output=ARTIFACTS_DIR + 'LowCode.CompareContextDocuments.docx').execute()
```

Shows how to compare documents from the stream using context.

```python
# There is a several ways to compare documents from the stream:
with system_helper.io.FileStream(MY_DIR + 'Table column bookmarks.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as first_stream_in:
    with system_helper.io.FileStream(MY_DIR + 'Table column bookmarks.doc', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as second_stream_in:
        comparer_context = aw.lowcode.ComparerContext()
        comparer_context.compare_options.ignore_case_changes = True
        comparer_context.author = 'Author'
        comparer_context.date_time = datetime.datetime(1, 1, 1)
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.CompareContextStreamDocuments.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            aw.lowcode.Comparer.create(comparer_context).from_stream(input=first_stream_in).from_stream(input=second_stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../)
* class [ProcessorContext](../processorcontext/)

