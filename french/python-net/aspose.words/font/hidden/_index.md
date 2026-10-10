---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /fr/python-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Examples

Shows how to create a run of hidden text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Avec le drapeau Hidden réglé sur true, tout texte que nous créons en utilisant cet objet Font sera invisible dans le document.
# Nous ne verrons pas ou ne mettrons pas en surbrillance le texte masqué à moins d'activer l'option "Hidden text"
# trouvée dans Microsoft Word via "File" -> "Options" -> "Display". Le texte sera toujours présent,
# et nous pourrons accéder à ce texte de manière programmatique.
# Il n'est pas recommandé d'utiliser cette méthode pour masquer des informations sensibles.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

