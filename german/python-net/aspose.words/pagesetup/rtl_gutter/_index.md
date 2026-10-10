---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /de/python-net/aspose.words/pagesetup/rtl_gutter/
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

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

