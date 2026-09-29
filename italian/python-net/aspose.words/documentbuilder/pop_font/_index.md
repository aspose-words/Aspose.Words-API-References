---
title: DocumentBuilder.pop_font method
linktitle: pop_font method
articleTitle: pop_font method
second_title: Aspose.Words for Python
description: "DocumentBuilder.pop_font method. Retrieves character formatting previously saved on the stack."
type: docs
weight: 630
url: /it/python-net/aspose.words/documentbuilder/pop_font/
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
# Imposta la formattazione del carattere, poi scrivi il testo che precede il collegamento ipertestuale.
builder.font.name = 'Arial'
builder.font.size = 24
builder.write('To visit Google, hold Ctrl and click ')
# Conserva la nostra configurazione di formattazione corrente nello stack.
builder.push_font()
# Modifica la formattazione corrente del builder applicando un nuovo stile.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink('here', 'http://www.google.com', False)
self.assertEqual(aspose.pydrawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)
# Ripristina la formattazione del carattere che abbiamo salvato in precedenza e rimuovi l'elemento dallo stack.
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

