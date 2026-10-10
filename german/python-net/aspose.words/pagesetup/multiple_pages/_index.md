---
title: PageSetup.multiple_pages property
linktitle: multiple_pages property
articleTitle: multiple_pages property
second_title: Aspose.Words for Python
description: "PageSetup.multiple_pages property. For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet."
type: docs
weight: 270
url: /de/python-net/aspose.words/pagesetup/multiple_pages/
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
# Fügen Sie Text ein, der sich über mehrere Seiten erstreckt.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Ein Bund fügt Leerzeichen entweder zum linken oder rechten Seitenrand hinzu,
# was die zentrale Falz von Buchseiten ausgleicht, die in das Layout der Seite eingreift.
page_setup = doc.sections[0].page_setup
# Bestimmen Sie, wie viel Platz unsere Seiten für Text innerhalb der Ränder haben, und fügen Sie dann einen Betrag hinzu, um einen Rand zu polstern.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Setzen Sie die Eigenschaft "RtlGutter" auf "true", um den Bund in eine besser geeignete Position für Rechts-nach-Links-Text zu platzieren.
page_setup.rtl_gutter = True
# Setzen Sie die Eigenschaft "MultiplePages" auf "MultiplePagesType.MirrorMargins", um zu wechseln
# die linke/rechte Seitenrandposition bei jeder Seite.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

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

