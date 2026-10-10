---
title: PageSetup.margins property
linktitle: margins property
articleTitle: margins property
second_title: Aspose.Words for Python
description: "PageSetup.margins property. Returns or sets preset [Margins](../../margins/) of the page."
type: docs
weight: 260
url: /sv/python-net/aspose.words/pagesetup/margins/
---

## PageSetup.margins property

Returns or sets preset [Margins](../../margins/) of the page.



```python
@property
def margins(self) -> aspose.words.Margins:
    ...

@margins.setter
def margins(self, value: aspose.words.Margins):
    ...

```

### Examples

Shows when to recalculate the page layout of the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Att spara ett dokument till PDF, till en bild eller skriva ut för första gången kommer automatiskt
# cacha layouten av dokumentet inom dess sidor.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Modifiera dokumentet på något sätt.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# I den nuvarande versionen av Aspose.Words återuppbyggs inte dokumentet automatiskt när det modifieras
# den cachade sidlayouten. Om vi vill att den cachade layouten
# ska hållas uppdaterad, måste vi uppdatera den manuellt.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

