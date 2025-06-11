---
title: SaveOutputParameters class
linktitle: SaveOutputParameters class
articleTitle: SaveOutputParameters class
second_title: Aspose.Words for Python
description: "aspose.words.saving.SaveOutputParameters class. This object is returned to the caller after a document is saved and contains additional information that  has been generated or calculated during the save operation"
type: docs
weight: 810
url: /python-net/aspose.words.saving/saveoutputparameters/
---

## SaveOutputParameters class

This object is returned to the caller after a document is saved and contains additional information that 
has been generated or calculated during the save operation. The caller can use or ignore this object.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [content_type](./content_type/) | Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document. |

### Examples

Shows how to access output parameters of a document's save operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
parameters = doc.save(file_name=ARTIFACTS_DIR + 'Document.SaveOutputParameters.doc')
self.assertEqual('application/msword', parameters.content_type)
# This property changes depending on the save format.
parameters = doc.save(file_name=ARTIFACTS_DIR + 'Document.SaveOutputParameters.pdf')
self.assertEqual('application/pdf', parameters.content_type)
```

### See Also

* module [aspose.words.saving](../)

