---
title: Font.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "Font.clear_formatting method. Resets to default font formatting."
type: docs
weight: 560
url: /es/python-net/aspose.words/font/clear_formatting/
---

## clear_formatting() {#default}

Resets to default font formatting.


```python
def clear_formatting(self):
    ...
```

### Remarks

Removes all font formatting specified explicitly on the object from which
[Font](../) was obtained so the font formatting will be inherited from
the appropriate parent.




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

### See Also

* module [aspose.words](../../)
* class [Font](../)

