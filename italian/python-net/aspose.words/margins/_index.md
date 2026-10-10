---
title: Margins enumeration
linktitle: Margins enumeration
articleTitle: Margins enumeration
second_title: Aspose.Words for Python
description: "aspose.words.Margins enumeration. Specifies preset margins."
type: docs
weight: 760
url: /it/python-net/aspose.words/margins/
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
# Salvare un documento in PDF, in un'immagine o stamparlo per la prima volta lo farà automaticamente
# memorizzare nella cache il layout del documento all'interno delle sue pagine.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Modificare il documento in qualche modo.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# Nella versione corrente di Aspose.Words, modificare il documento non ricostruisce automaticamente
# il layout della pagina memorizzato nella cache. Se desideriamo che il layout memorizzato nella cache
# rimanga aggiornato, dovremo aggiornarlo manualmente.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

### See Also

* module [aspose.words](../)

