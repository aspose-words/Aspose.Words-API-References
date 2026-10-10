---
title: Margins enumeration
linktitle: Margins enumeration
articleTitle: Margins enumeration
second_title: Aspose.Words for Python
description: "aspose.words.Margins enumeration. Specifies preset margins."
type: docs
weight: 760
url: /sv/python-net/aspose.words/margins/
---

## Margins enumeration

Specifies preset margins.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Normal margins. |
| NARROW | Narrow margins. |
| MODERATE | Moderate margins. |
| WIDE | Wide margins. |
| MIRRORED | Mirrored margins. |
| CUSTOM | Custom margins. |

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

* module [aspose.words](../)

