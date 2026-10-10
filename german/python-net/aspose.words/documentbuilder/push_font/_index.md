---
title: DocumentBuilder.push_font method
linktitle: push_font method
articleTitle: push_font method
second_title: Aspose.Words for Python
description: "DocumentBuilder.push_font method. Saves current character formatting onto the stack."
type: docs
weight: 640
url: /de/python-net/aspose.words/documentbuilder/push_font/
---

## push_font() {#default}

Saves current character formatting onto the stack.


```python
def push_font(self):
    ...
```

### Examples

Shows how to use a document builder's formatting stack.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Richten Sie die Schriftformatierung ein und schreiben Sie dann den Text, der vor dem Hyperlink steht.
builder.font.name = 'Arial'
builder.font.size = 24
builder.write('To visit Google, hold Ctrl and click ')
# Bewahren Sie unsere aktuelle Formatierungskonfiguration im Stack auf.
builder.push_font()
# Ändern Sie die aktuelle Formatierung des Builders, indem Sie einen neuen Stil anwenden.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink('here', 'http://www.google.com', False)
self.assertEqual(aspose.pydrawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)
# Stellen Sie die zuvor gespeicherte Schriftformatierung wieder her und entfernen Sie das Element aus dem Stack.
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
* method [DocumentBuilder.pop_font()](../pop_font/#default)

