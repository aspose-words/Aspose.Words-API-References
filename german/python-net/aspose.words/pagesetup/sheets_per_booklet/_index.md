---
title: PageSetup.sheets_per_booklet property
linktitle: sheets_per_booklet property
articleTitle: sheets_per_booklet property
second_title: Aspose.Words for Python
description: "PageSetup.sheets_per_booklet property. Returns or sets the number of pages to be included in each booklet."
type: docs
weight: 400
url: /de/python-net/aspose.words/pagesetup/sheets_per_booklet/
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
# Fügen Sie Text ein, der sich über 16 Seiten erstreckt.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Konfigurieren Sie die "PageSetup"-Eigenschaft des ersten Abschnitts, um das Dokument in Form eines Buchfalz zu drucken.
# Wenn wir dieses Dokument beidseitig drucken, können wir die Seiten nehmen, um sie zu stapeln
# und sie alle gleichzeitig in der Mitte zu falten. Der Inhalt des Dokuments wird zu einem Buchfalz ausgerichtet.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Wir können die Anzahl der Blätter nur in Vielfachen von 4 angeben.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

