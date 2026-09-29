---
title: PageSetup.gutter property
linktitle: gutter property
articleTitle: gutter property
second_title: Aspose.Words for Python
description: "PageSetup.gutter property. Gets or sets the amount of extra space added to the margin for document binding."
type: docs
weight: 160
url: /it/python-net/aspose.words/pagesetup/gutter/
---

## PageSetup.gutter property

Gets or sets the amount of extra space added to the margin for document binding.


```python
@property
def gutter(self) -> float:
    ...

@gutter.setter
def gutter(self, value: float):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# Inserisci del testo che si estende su più pagine.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Una rilegatura aggiunge spazi bianchi al margine sinistro o destro della pagina,
# compensando la piega centrale delle pagine di un libro che invade il layout della pagina.
page_setup = doc.sections[0].page_setup
# Determina quanto spazio hanno le nostre pagine per il testo all'interno dei margini e poi aggiungi una quantità per imbottire un margine.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Imposta la proprietà "RtlGutter" su "true" per posizionare la rilegatura in una posizione più adatta al testo da destra a sinistra.
page_setup.rtl_gutter = True
# Imposta la proprietà "MultiplePages" su "MultiplePagesType.MirrorMargins" per alternare
# la posizione laterale sinistra/destra dei margini per ogni pagina.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

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

* module [aspose.words](../../)
* class [PageSetup](../)

