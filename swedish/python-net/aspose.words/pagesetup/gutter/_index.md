---
title: PageSetup.gutter property
linktitle: gutter property
articleTitle: gutter property
second_title: Aspose.Words for Python
description: "PageSetup.gutter property. Gets or sets the amount of extra space added to the margin for document binding."
type: docs
weight: 160
url: /sv/python-net/aspose.words/pagesetup/gutter/
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
# Infoga text som sträcker sig över flera sidor.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# En gutter lägger till blanksteg antingen till den vänstra eller högra sidmarginalen,
# vilket kompenserar för den centrala vikningen av sidor i en bok som inkräktar på sidans layout.
page_setup = doc.sections[0].page_setup
# Bestäm hur mycket utrymme våra sidor har för text inom marginalerna och lägg sedan till ett värde för att fylla ut en marginal.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Ställ in egenskapen "RtlGutter" till "true" för att placera guttern i en mer lämplig position för höger‑till‑vänster‑text.
page_setup.rtl_gutter = True
# Ställ in egenskapen "MultiplePages" till "MultiplePagesType.MirrorMargins" för att växla
# vänster/höger sidposition för marginaler på varje sida.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# Infoga text som sträcker sig över 16 sidor.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Konfigurera den första sektionens egenskap "PageSetup" för att skriva ut dokumentet i form av en bokvikt.
# När vi skriver ut detta dokument på båda sidor kan vi ta sidorna för att stapla dem
# och vika dem alla ner i mitten på en gång. Dokumentets innehåll kommer att radas upp till en bokvikt.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Vi kan endast ange antalet ark i multiplar av 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

