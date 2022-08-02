---
title: SaveOutputParameters class
second_title: Aspose.Words for Python via .NET API Reference
description: "This object is returned to the caller after a document is saved and contains additional information that  has been generated or calculated during the save operation"
type: docs
weight: 720
url: /python-net/aspose.words.saving/saveoutputparameters/
---

## SaveOutputParameters class

This object is returned to the caller after a document is saved and contains additional information that 
has been generated or calculated during the save operation. The caller can use or ignore this object.


### Properties

| Name | Description |
| --- | --- |
| [content_type](./content_type/) | Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document. |

### Examples

Shows how to access output parameters of a document's save operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
parameters = doc.save(ARTIFACTS_DIR + "Document.save_output_parameters.doc")

self.assertEqual("application/msword", parameters.content_type)

# This property changes depending on the save format.
parameters = doc.save(ARTIFACTS_DIR + "Document.save_output_parameters.pdf")

self.assertEqual("application/pdf", parameters.content_type)
```

### See Also

* module [aspose.words.saving](../)

