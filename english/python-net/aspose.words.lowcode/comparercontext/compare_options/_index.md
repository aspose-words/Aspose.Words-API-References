---
title: ComparerContext.compare_options property
linktitle: compare_options property
articleTitle: compare_options property
second_title: Aspose.Words for Python
description: "ComparerContext.compare_options property. Options used upon comparing documents."
type: docs
weight: 40
url: /python-net/aspose.words.lowcode/comparercontext/compare_options/
---

## ComparerContext.compare_options property

Options used upon comparing documents.


```python
@property
def compare_options(self) -> aspose.words.comparing.CompareOptions:
    ...

```

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

* module [aspose.words.lowcode](../../)
* class [ComparerContext](../)

