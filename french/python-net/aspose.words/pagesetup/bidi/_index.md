---
title: PageSetup.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "PageSetup.bidi property. Specifies that this section contains bidirectional (complex scripts) text."
type: docs
weight: 10
url: /fr/python-net/aspose.words/pagesetup/bidi/
---

## PageSetup.bidi property

Specifies that this section contains bidirectional (complex scripts) text.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the columns in this section are laid out from right to left.




### Examples

Shows how to set the order of text columns in a section.

```python
doc = aw.Document()
page_setup = doc.sections[0].page_setup
page_setup.text_columns.set_count(3)
builder = aw.DocumentBuilder(doc=doc)
builder.write('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.write('Column 2.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.write('Column 3.')
# Définissez la propriété "Bidi" sur "true" pour disposer les colonnes en commençant par le côté droit de la page.
# L'ordre des colonnes correspondra à la direction du texte de droite à gauche.
# Définissez la propriété "Bidi" sur "false" pour disposer les colonnes en commençant par le côté gauche de la page.
# L'ordre des colonnes correspondra à la direction du texte de gauche à droite.
page_setup.bidi = reverse_columns
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

