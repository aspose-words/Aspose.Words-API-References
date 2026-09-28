---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /fr/python-net/aspose.words/pagesetup/rtl_gutter/
---

## PageSetup.rtl_gutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


```python
@property
def rtl_gutter(self) -> bool:
    ...

@rtl_gutter.setter
def rtl_gutter(self, value: bool):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# Insérez du texte qui s'étend sur plusieurs pages.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Une gouttière ajoute des espaces blancs à la marge de page gauche ou droite,
# ce qui compense le pli central des pages d'un livre qui empiète sur la mise en page.
page_setup = doc.sections[0].page_setup
# Déterminez l'espace disponible pour le texte dans les marges de nos pages, puis ajoutez une quantité pour rembourrer une marge.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Définissez la propriété "RtlGutter" à "true" pour placer la gouttière à une position plus adaptée au texte de droite à gauche.
page_setup.rtl_gutter = True
# Définissez la propriété "MultiplePages" à "MultiplePagesType.MirrorMargins" pour alterner
# la position côté gauche/droite des marges à chaque page.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

