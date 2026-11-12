---
title: PageSetup.margins property
linktitle: margins property
articleTitle: margins property
second_title: Aspose.Words for Python
description: "PageSetup.margins property. Returns or sets preset [Margins](../../margins/) of the page."
type: docs
weight: 260
url: /tr/python-net/aspose.words/pagesetup/margins/
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
# Bir belgeyi PDF olarak kaydetmek, bir görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
# belgenin sayfalarındaki yerleşimi önbelleğe alır.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Belgeyi bir şekilde değiştirin.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# Aspose.Words'ün mevcut sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
# önbelleğe alınmış sayfa yerleşimini. Önbelleğe alınmış yerleşimin
# güncel kalmasını istiyorsak, manuel olarak güncellememiz gerekir.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

