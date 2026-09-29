---
title: MultiplePagesType enumeration
linktitle: MultiplePagesType enumeration
articleTitle: MultiplePagesType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.MultiplePagesType enumeration. Specifies how document is printed out."
type: docs
weight: 110
url: /it/python-net/aspose.words.settings/multiplepagestype/
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
# Inserisci del testo che si estende su 16 pagine.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Configura la proprietà "PageSetup" della prima sezione per stampare il documento in forma di piega a libro.
# Quando stampiamo questo documento su entrambi i lati, possiamo prendere le pagine per impilarle
# e piegarle tutte a metà contemporaneamente. Il contenuto del documento si allineerà in una piega a libro.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Possiamo specificare il numero di fogli solo in multipli di 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words.settings](../)

