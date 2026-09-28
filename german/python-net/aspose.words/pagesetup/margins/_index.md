---
title: PageSetup.margins property
linktitle: margins property
articleTitle: margins property
second_title: Aspose.Words for Python
description: "PageSetup.margins property. Returns or sets preset [Margins](../../margins/) of the page."
type: docs
weight: 260
url: /de/python-net/aspose.words/pagesetup/margins/
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
# Das Speichern eines Dokuments als PDF, als Bild oder das erstmalige Drucken wird automatisch
# den Layout des Dokuments innerhalb seiner Seiten zwischenspeichern.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Das Dokument auf irgendeine Weise ändern.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# In der aktuellen Version von Aspose.Words führt das Ändern des Dokuments nicht automatisch zu einem Neuaufbau
# des zwischengespeicherten Seitenlayouts. Wenn wir möchten, dass das zwischengespeicherte Layout
# auf dem neuesten Stand bleibt, müssen wir es manuell aktualisieren.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

