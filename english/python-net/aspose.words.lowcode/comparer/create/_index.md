---
title: Comparer.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Comparer.create method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/comparer/create/
---

## create() {#default}

Creates new instance of the converter processor.


```python
def create(self):
    ...
```

## create(context) {#comparercontext}

Creates new instance of the comparer processor.


```python
def create(self, context: aspose.words.lowcode.ComparerContext):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| context | [ComparerContext](../../comparercontext/) |  |

## Examples

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

## See Also

* module [aspose.words.lowcode](../../)
* class [Comparer](../)

