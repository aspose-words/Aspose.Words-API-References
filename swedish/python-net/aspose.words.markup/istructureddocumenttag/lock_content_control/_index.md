---
title: IStructuredDocumentTag.lock_content_control property
linktitle: lock_content_control property
articleTitle: lock_content_control property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.lock_content_control property. When set to true, this property will prohibit a user from deleting this SDT."
type: docs
weight: 70
url: /sv/python-net/aspose.words.markup/istructureddocumenttag/lock_content_control/
---

## IStructuredDocumentTag.lock_content_control property

When set to true, this property will prohibit a user from deleting this **SDT**.



```python
@property
def lock_content_control(self) -> bool:
    ...

@lock_content_control.setter
def lock_content_control(self, value: bool):
    ...

```

### Examples

Shows how to apply editing restrictions to structured document tags.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga en strukturerad dokumenttagg med vanlig text, som fungerar som en textruta som uppmanar användaren att fylla i den.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Ställ in egenskapen "LockContents" till "true" för att förhindra att användaren redigerar innehållet i denna textruta.
tag.lock_contents = True
builder.write('The contents of this structured document tag cannot be edited: ')
builder.insert_node(tag)
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Ställ in egenskapen "LockContentControl" till "true" för att förhindra att användaren från
# raderar denna strukturerade dokumenttagg manuellt i Microsoft Word.
tag.lock_content_control = True
builder.insert_paragraph()
builder.write('This structured document tag cannot be deleted but its contents can be edited: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.Lock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

