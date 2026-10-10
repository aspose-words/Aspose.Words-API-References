---
title: Font.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "Font.clear_formatting method. Resets to default font formatting."
type: docs
weight: 560
url: /it/python-net/aspose.words/font/clear_formatting/
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
# Inserisci un collegamento ipertestuale e enfatizzalo con una formattazione personalizzata.
# Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# Ctrl + clic sinistro sul collegamento nel testo in Microsoft Word ci porterà all'URL tramite una nuova finestra del browser web.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

