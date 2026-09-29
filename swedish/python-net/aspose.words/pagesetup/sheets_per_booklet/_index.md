---
title: PageSetup.sheets_per_booklet property
linktitle: sheets_per_booklet property
articleTitle: sheets_per_booklet property
second_title: Aspose.Words for Python
description: "PageSetup.sheets_per_booklet property. Returns or sets the number of pages to be included in each booklet."
type: docs
weight: 400
url: /sv/python-net/aspose.words/pagesetup/sheets_per_booklet/
---

## PageSetup.sheets_per_booklet property

Returns or sets the number of pages to be included in each booklet.


```python
@property
def sheets_per_booklet(self) -> int:
    ...

@sheets_per_booklet.setter
def sheets_per_booklet(self, value: int):
    ...

```

### Examples

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

