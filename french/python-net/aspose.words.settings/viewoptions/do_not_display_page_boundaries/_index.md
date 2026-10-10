---
title: ViewOptions.do_not_display_page_boundaries property
linktitle: do_not_display_page_boundaries property
articleTitle: do_not_display_page_boundaries property
second_title: Aspose.Words for Python
description: "ViewOptions.do_not_display_page_boundaries property. Turns off display of the space between the top of the text and the top edge of the page."
type: docs
weight: 20
url: /fr/python-net/aspose.words.settings/viewoptions/do_not_display_page_boundaries/
---

## ViewOptions.do_not_display_page_boundaries property

Turns off display of the space between the top of the text and the top edge of the page.


```python
@property
def do_not_display_page_boundaries(self) -> bool:
    ...

@do_not_display_page_boundaries.setter
def do_not_display_page_boundaries(self, value: bool):
    ...

```

### Examples

Shows how to hide vertical whitespace and headers/footers in view options.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez du contenu qui s'étend sur 3 pages.
builder.writeln('Paragraph 1, Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Paragraph 2, Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Paragraph 3, Page 3.')
# Insérez un en-tête et un pied de page.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('This is the header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('This is the footer.')
# Ce document contient une petite quantité de contenu qui occupe l'équivalent de quelques pages complètes.
# Définissez le drapeau "DoNotDisplayPageBoundaries" sur "true" pour que les anciennes versions de Microsoft Word omettent les en-têtes,
# les pieds de page, et une grande partie des espaces blancs verticaux lors de l'affichage de notre document.
# Définissez le drapeau "DoNotDisplayPageBoundaries" sur "false" pour que les anciennes versions de Microsoft Word
# pour afficher normalement notre document.
doc.view_options.do_not_display_page_boundaries = do_not_display_page_boundaries
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayPageBoundaries.doc')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

