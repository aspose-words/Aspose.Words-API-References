---
title: Font.no_proofing property
linktitle: no_proofing property
articleTitle: no_proofing property
second_title: Aspose.Words for Python
description: "Font.no_proofing property. True when the formatted characters are not to be spell checked."
type: docs
weight: 280
url: /es/python-net/aspose.words/font/no_proofing/
---

## Font.no_proofing property

True when the formatted characters are not to be spell checked.


```python
@property
def no_proofing(self) -> bool:
    ...

@no_proofing.setter
def no_proofing(self, value: bool):
    ...

```

### Examples

Shows how to prevent text from being spell checked by Microsoft Word.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Normalmente, Microsoft Word resalta los errores ortográficos con una subrayado rojo irregular.
# Podemos desactivar la bandera "NoProofing" para crear una porción de texto que
# omita el corrector ortográfico mientras lo desactiva por completo.
builder.font.no_proofing = True
builder.writeln('Proofing has been disabled, so these spelking errrs will not display red lines underneath.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NoProofing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

