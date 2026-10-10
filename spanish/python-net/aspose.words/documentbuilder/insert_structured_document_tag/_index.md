---
title: DocumentBuilder.insert_structured_document_tag method
linktitle: insert_structured_document_tag method
articleTitle: insert_structured_document_tag method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_structured_document_tag method. Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document."
type: docs
weight: 480
url: /es/python-net/aspose.words/documentbuilder/insert_structured_document_tag/
---

## insert_structured_document_tag(type) {#sdttype}

Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document.



```python
def insert_structured_document_tag(self, type: aspose.words.markup.SdtType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [SdtType](../../../aspose.words.markup/sdttype/) |  |

### Returns

The [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node that was just inserted.


### Examples

Shows how to simply insert structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to(doc.first_section.body.paragraphs[3])
# Nota, que solo se permiten los siguientes tipos de StructuredDocumentTag para inserción:
# SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
# SdtType.ComboBox, SdtType.Picture, SdtType.Date.
# El nivel de marcado del StructuredDocumentTag insertado se detectará automáticamente y depende de la posición en la que se inserta.
# El StructuredDocumentTag añadido heredará el formato de párrafo y fuente desde la posición del cursor.
sdt_plain = builder.insert_structured_document_tag(aw.markup.SdtType.PLAIN_TEXT)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.InsertStructuredDocumentTag.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

