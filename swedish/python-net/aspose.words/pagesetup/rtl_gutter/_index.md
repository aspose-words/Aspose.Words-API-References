---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /sv/python-net/aspose.words/pagesetup/rtl_gutter/
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

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

