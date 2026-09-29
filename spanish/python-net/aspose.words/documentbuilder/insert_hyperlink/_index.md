---
title: DocumentBuilder.insert_hyperlink method
linktitle: insert_hyperlink method
articleTitle: insert_hyperlink method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_hyperlink method. Inserts a hyperlink into the document."
type: docs
weight: 390
url: /es/python-net/aspose.words/documentbuilder/insert_hyperlink/
---

## insert_hyperlink(display_text, url_or_bookmark, is_bookmark) {#str_str_bool}

Inserts a hyperlink into the document.


```python
def insert_hyperlink(self, display_text: str, url_or_bookmark: str, is_bookmark: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| display_text | str | Text of the link to be displayed in the document. |
| url_or_bookmark | str | Link destination. Can be a url or a name of a bookmark inside the document. This method always adds apostrophes at the beginning and end of the url. |
| is_bookmark | bool | ``True`` if the previous parameter is a name of a bookmark inside the document; ``False`` is the previous parameter is a URL. |

### Remarks

Note that you need to specify font formatting for the hyperlink display text explicitly
using the [DocumentBuilder.font](../font/) property.

This methods internally calls [DocumentBuilder.insert_field()](../insert_field/#str) to insert an MS Word HYPERLINK field
into the document.




### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.


### Examples

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('For more information, please visit the ')
# Inserte un hipervínculo y enfatícelo con formato personalizado.
# El hipervínculo será un fragmento de texto clicable que nos llevará a la ubicación especificada en la URL.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL mediante una nueva ventana del navegador.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

Shows how to use a document builder's formatting stack.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Configure el formato de fuente, luego escriba el texto que precede al hipervínculo.
builder.font.name = 'Arial'
builder.font.size = 24
builder.write('To visit Google, hold Ctrl and click ')
# Conserve nuestra configuración de formato actual en la pila.
builder.push_font()
# Modifique el formato actual del builder aplicando un nuevo estilo.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink('here', 'http://www.google.com', False)
self.assertEqual(aspose.pydrawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)
# Restaure el formato de fuente que guardamos anteriormente y elimine el elemento de la pila.
builder.pop_font()
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.NONE, builder.font.underline)
builder.write('. We hope you enjoyed the example.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.PushPopFont.docx')
```

Shows how to insert a hyperlink which references a local bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('Bookmark1')
builder.write('Bookmarked text. ')
builder.end_bookmark('Bookmark1')
builder.writeln('Text outside of the bookmark.')
# Inserte un campo HYPERLINK que enlace al marcador. Podemos pasar interruptores de campo
# al método "InsertHyperlink" como parte del argumento que contiene el nombre del marcador referenciado.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
hyperlink = builder.insert_hyperlink('Link to Bookmark1', 'Bookmark1', True).as_field_hyperlink()
hyperlink.screen_tip = 'Hyperlink Tip'
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlinkToLocalBookmark.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

