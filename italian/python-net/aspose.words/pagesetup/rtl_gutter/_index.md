---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /it/python-net/aspose.words/pagesetup/rtl_gutter/
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

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

