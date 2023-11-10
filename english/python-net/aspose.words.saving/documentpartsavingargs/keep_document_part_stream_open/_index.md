---
title: DocumentPartSavingArgs.keep_document_part_stream_open property
linktitle: keep_document_part_stream_open property
articleTitle: keep_document_part_stream_open property
second_title: Aspose.Words for Python
description: "DocumentPartSavingArgs.keep_document_part_stream_open property. Specifies whether Aspose.Words should keep the stream open or close it after saving a document part."
type: docs
weight: 40
url: /python-net/aspose.words.saving/documentpartsavingargs/keep_document_part_stream_open/
---

## DocumentPartSavingArgs.keep_document_part_stream_open property

Specifies whether Aspose.Words should keep the stream open or close it after saving a document part.


```python
@property
def keep_document_part_stream_open(self) -> bool:
    ...

@keep_document_part_stream_open.setter
def keep_document_part_stream_open(self, value: bool):
    ...

```

### Remarks

Default is ``False`` and Aspose.Words will close the stream you provided
in the [DocumentPartSavingArgs.document_part_stream](../document_part_stream/) property after writing a document part into it.
Specify ``True`` to keep the stream open. Please note that the main output stream 
provided in the call to [Document.save()](../../../aspose.words/document/save/#bytesio_saveformat) or 
[Document.save()](../../../aspose.words/document/save/#bytesio_saveoptions) will never be closed by Aspose.Words 
even if [DocumentPartSavingArgs.keep_document_part_stream_open](./) is set to ``False``.




### See Also

* module [aspose.words.saving](../../)
* class [DocumentPartSavingArgs](../)
* property [DocumentPartSavingArgs.document_part_stream](../document_part_stream/)

