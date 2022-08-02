---
title: content_type property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document."
type: docs
weight: 10
url: /python-net/aspose.words.saving/saveoutputparameters/content_type/
---

## SaveOutputParameters.content_type property

Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document.


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

* module [aspose.words.saving](../../)
* class [SaveOutputParameters](../)

