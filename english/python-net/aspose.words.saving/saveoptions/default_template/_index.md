---
title: default_template property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets path to default template (including filename)"
type: docs
weight: 20
url: /python-net/aspose.words.saving/saveoptions/default_template/
---

## SaveOptions.default_template property

Gets or sets path to default template (including filename).
Default value for this property is **empty string** (System.String.Empty).


If specified, this path is used to load template when [Document.automatically_update_styles](../../../aspose.words/document/automatically_update_styles/) is ``True``,
but [Document.attached_template](../../../aspose.words/document/attached_template/) is empty.


### Examples

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

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

