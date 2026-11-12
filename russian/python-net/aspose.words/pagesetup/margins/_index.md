---
title: PageSetup.margins property
linktitle: margins property
articleTitle: margins property
second_title: Aspose.Words for Python
description: "PageSetup.margins property. Returns or sets preset [Margins](../../margins/) of the page."
type: docs
weight: 260
url: /ru/python-net/aspose.words/pagesetup/margins/
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
# Сохранение документа в PDF, в изображение или печать в первый раз будет автоматически
# кешировать макет документа внутри его страниц.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Измените документ каким-либо образом.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# В текущей версии Aspose.Words изменение документа не приводит к автоматическому пересозданию
# кешированного макета страниц. Если мы хотим, чтобы кешированный макет
# оставался актуальным, нам придётся обновлять его вручную.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

