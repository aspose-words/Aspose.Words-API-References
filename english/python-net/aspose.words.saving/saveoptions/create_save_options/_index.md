---
title: create_save_options method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.saving.SaveOptions.create_save_options method"
type: docs
weight: 200
url: /python-net/aspose.words.saving/saveoptions/create_save_options/
---

## create_save_options(save_format) {#saveformat}

Creates a save options object of a class suitable for the specified save format.


```python
def create_save_options(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

### Returns

An object of a class that derives from [SaveOptions](../).


## create_save_options(file_name) {#str}

Creates a save options object of a class suitable for the file extension specified in the given file name.


```python
def create_save_options(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

### Returns

An object of a class that derives from [SaveOptions](../).


## Examples

Shows an option to optimize memory consumption when rendering large documents to PDF.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.SaveOptions.create_save_options(aw.SaveFormat.PDF)

# Set the "memory_optimization" property to "True" to lower the memory footprint of large documents' saving operations
# at the cost of increasing the duration of the operation.
# Set the "memory_optimization" property to "False" to save the document as a PDF normally.
save_options.memory_optimization = memory_optimization

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.memory_optimization.pdf", save_options)
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()

# Enable automatic style updating, but do not attach a template document.
doc.automatically_update_styles = True

self.assertEqual("", doc.attached_template)

# Since there is no template document, the document had nowhere to track style changes.
# Use a SaveOptions object to automatically set a template
# if a document that we are saving does not have one.
options = aw.saving.SaveOptions.create_save_options("Document.default_template.docx")
options.default_template = MY_DIR + "Business brochure.dotx"

doc.save(ARTIFACTS_DIR + "Document.default_template.docx", options)
```

## See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

