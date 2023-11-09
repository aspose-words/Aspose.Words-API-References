---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /python-net/aspose.words.loading/txtloadoptions/document_direction/
---

## TxtLoadOptions.document_direction property

Gets or sets a document direction.
The default value is [DocumentDirection.LEFT_TO_RIGHT](../../documentdirection/#LEFT_TO_RIGHT).



```python
@property
def document_direction(self) -> aspose.words.loading.DocumentDirection:
    ...

@document_direction.setter
def document_direction(self, value: aspose.words.loading.DocumentDirection):
    ...

```

### Examples

Shows how to detect plaintext document text direction.

```python
# Create a "TxtLoadOptions" object, which we can pass to a document's constructor
# to modify how we load a plaintext document.
load_options = aw.loading.TxtLoadOptions()

# Set the "document_direction" property to "DocumentDirection.AUTO" automatically detects
# the direction of every paragraph of text that Aspose.Words loads from plaintext.
# Each paragraph's "bidi" property will store its direction.
load_options.document_direction = aw.loading.DocumentDirection.AUTO

# Detect Hebrew text as right-to-left.
doc = aw.Document(MY_DIR + "Hebrew text.txt", load_options)

self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)

# Detect English text as right-to-left.
doc = aw.Document(MY_DIR + "English text.txt", load_options)

self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

