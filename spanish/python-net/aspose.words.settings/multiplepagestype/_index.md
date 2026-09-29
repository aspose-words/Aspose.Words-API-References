---
title: MultiplePagesType enumeration
linktitle: MultiplePagesType enumeration
articleTitle: MultiplePagesType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.MultiplePagesType enumeration. Specifies how document is printed out."
type: docs
weight: 110
url: /es/python-net/aspose.words.settings/multiplepagestype/
---

## MultiplePagesType enumeration

Specifies how document is printed out.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Normal printing, no multiple pages specified. |
| MIRROR_MARGINS | Swaps left and right margins on facing pages. |
| TWO_PAGES_PER_SHEET | Prints two pages per sheet. |
| BOOK_FOLD_PRINTING | Specifies whether to print the document as a book fold. |
| BOOK_FOLD_PRINTING_REVERSE | Specifies whether to print the document as a reverse book fold. |
| DEFAULT | Default value is [MultiplePagesType.NORMAL](./#NORMAL) |

### Examples

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# Inserte texto que abarque 16 páginas.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de pliegue de libro.
# Cuando imprimimos este documento a doble cara, podemos tomar las páginas para apilarlas
# y doblarlas todas por la mitad de una vez. El contenido del documento se alineará en un pliegue de libro.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Solo podemos especificar el número de hojas en múltiplos de 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words.settings](../)

