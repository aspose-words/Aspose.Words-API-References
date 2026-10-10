---
title: PageSetup.margins property
linktitle: margins property
articleTitle: margins property
second_title: Aspose.Words for Python
description: "PageSetup.margins property. Returns or sets preset [Margins](../../margins/) of the page."
type: docs
weight: 260
url: /zh/python-net/aspose.words/pagesetup/margins/
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
# 首次将文档保存为 PDF、图像或进行打印时，将自动
# 缓存文档在各页中的布局。
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# 以某种方式修改文档。
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# 在当前版本的 Aspose.Words 中，修改文档不会自动重建
# 缓存的页面布局。如果我们希望缓存的布局
# 保持最新，需要手动更新它。
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

