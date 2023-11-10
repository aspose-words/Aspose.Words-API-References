---
title: StructuredDocumentTag.lock_contents property
linktitle: lock_contents property
articleTitle: lock_contents property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.lock_contents property. When set to ``True``, this property will prohibit a user from editing the contents of this SDT."
type: docs
weight: 200
url: /python-net/aspose.words.markup/structureddocumenttag/lock_contents/
---

## StructuredDocumentTag.lock_contents property

When set to ``True``, this property will prohibit a user from editing the contents of this **SDT**.



```python
@property
def lock_contents(self) -> bool:
    ...

@lock_contents.setter
def lock_contents(self, value: bool):
    ...

```

### Examples

Shows how to apply editing restrictions to structured document tags.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)

# Set the "lock_contents" property to "True" to prohibit the user from editing this text box's contents.
tag.lock_contents = True
builder.write("The contents of this structured document tag cannot be edited: ")
builder.insert_node(tag)

tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)

# Set the "lock_content_control" property to "True" to prohibit the user from
# deleting this structured document tag manually in Microsoft Word.
tag.lock_content_control = True

builder.insert_paragraph()
builder.write("This structured document tag cannot be deleted but its contents can be edited: ")
builder.insert_node(tag)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.lock.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

