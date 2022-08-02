---
title: automatically_update_styles property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /python-net/aspose.words/document/automatically_update_styles/
---

## Document.automatically_update_styles property

Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the
attached template each time the document is opened in MS Word.


### Examples

Shows how to attach a template to a document.

```python
doc = aw.Document()

# Microsoft Word documents by default come with an attached template called "Normal.dotm".
# There is no default template for blank Aspose.Words documents.
self.assertEqual("", doc.attached_template)

# Attach a template, then set the flag to apply style changes
# within the template to styles in our document.
doc.attached_template = MY_DIR + "Business brochure.dotx"
doc.automatically_update_styles = True

doc.save(ARTIFACTS_DIR + "Document.automatically_update_styles.docx")
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

### See Also

* module [aspose.words](../../)
* class [Document](../)

