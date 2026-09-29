---
title: DocumentBuilder.pop_font method
linktitle: pop_font method
articleTitle: pop_font method
second_title: Aspose.Words for Python
description: "DocumentBuilder.pop_font method. Retrieves character formatting previously saved on the stack."
type: docs
weight: 630
url: /sv/python-net/aspose.words/documentbuilder/pop_font/
---

## pop_font() {#default}

Retrieves character formatting previously saved on the stack.


```python
def pop_font(self):
    ...
```

### Examples

Shows how to use a document builder's formatting stack.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ställ in teckensnittsformatering, skriv sedan texten som kommer före hyperlänken.
builder.font.name = 'Arial'
builder.font.size = 24
builder.write('To visit Google, hold Ctrl and click ')
# Bevara vår nuvarande formateringskonfiguration på stacken.
builder.push_font()
# Ändra byggarens aktuella formatering genom att tillämpa en ny stil.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink('here', 'http://www.google.com', False)
self.assertEqual(aspose.pydrawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)
# Återställ teckensnittsformateringen som vi sparade tidigare och ta bort elementet från stacken.
builder.pop_font()
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.NONE, builder.font.underline)
builder.write('. We hope you enjoyed the example.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.PushPopFont.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)
* property [DocumentBuilder.font](../font/)
* method [DocumentBuilder.push_font()](../push_font/#default)

