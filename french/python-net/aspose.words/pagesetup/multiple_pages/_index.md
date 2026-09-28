---
title: PageSetup.multiple_pages property
linktitle: multiple_pages property
articleTitle: multiple_pages property
second_title: Aspose.Words for Python
description: "PageSetup.multiple_pages property. For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet."
type: docs
weight: 270
url: /fr/python-net/aspose.words/pagesetup/multiple_pages/
---

## PageSetup.multiple_pages property

For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.


```python
@property
def multiple_pages(self) -> aspose.words.settings.MultiplePagesType:
    ...

@multiple_pages.setter
def multiple_pages(self, value: aspose.words.settings.MultiplePagesType):
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

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# Insérez du texte qui s'étend sur 16 pages.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Configurez la propriété "PageSetup" de la première section pour imprimer le document sous forme de pliage de livre.
# Lorsque nous imprimons ce document des deux côtés, nous pouvons prendre les pages pour les empiler
# et les plier toutes au milieu en une fois. Le contenu du document s'alignera en un pliage de livre.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Nous ne pouvons spécifier le nombre de feuilles qu'en multiples de 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

