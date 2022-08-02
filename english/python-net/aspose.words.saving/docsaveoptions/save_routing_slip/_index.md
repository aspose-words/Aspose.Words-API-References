---
title: save_routing_slip property
second_title: Aspose.Words for Python via .NET API Reference
description: "When ``false``, RoutingSlip data is not saved to output document"
type: docs
weight: 60
url: /python-net/aspose.words.saving/docsaveoptions/save_routing_slip/
---

## DocSaveOptions.save_routing_slip property

When ``false``, RoutingSlip data is not saved to output document.
Default value is **true**.



### Examples

Shows how to set save options for older Microsoft Word formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write("Hello world!")

options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)

# Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
# Note that this does not encrypt the contents of the document in any way.
options.password = "MyPassword"

# If the document contains a routing slip, we can preserve it while saving by setting this flag to True.
options.save_routing_slip = True

doc.save(ARTIFACTS_DIR + "DocSaveOptions.save_as_doc.doc", options)

# To be able to load the document,
# we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
with self.assertRaises(Exception):
    doc = aw.Document(ARTIFACTS_DIR + "DocSaveOptions.save_as_doc.doc")

load_options = aw.loading.LoadOptions("MyPassword")
doc = aw.Document(ARTIFACTS_DIR + "DocSaveOptions.save_as_doc.doc", load_options)

self.assertEqual("Hello world!", doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

