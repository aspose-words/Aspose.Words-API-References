---
title: PageSet.odd property
linktitle: odd property
articleTitle: odd property
second_title: Aspose.Words for Python
description: "PageSet.odd property. Gets a set with all the odd pages of the document in their original order."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/pageset/odd/
---

## PageSet.odd property

Gets a set with all the odd pages of the document in their original order.


```python
@property
def odd(self) -> aspose.words.saving.PageSet:
    ...

```

### Remarks

Odd pages have even indices since page indices are zero-based.


### Examples

Shows how to export Odd pages from the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 5:
    builder.writeln(f"Page {i + 1} ({('odd' if i % 2 == 0 else 'even')})")
    if i < 4:
        builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 以下是三个 PageSet 属性，我们可以用它们从
# 我们的文档中筛选页面，以基于页码的奇偶性保存到输出的 PDF 文档中。
# 1 - 仅保存偶数页：
options.page_set = aw.saving.PageSet.even
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Even.pdf', save_options=options)
# 2 - 仅保存奇数页：
options.page_set = aw.saving.PageSet.odd
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Odd.pdf', save_options=options)
# 3 -  保存每页：
options.page_set = aw.saving.PageSet.all
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.All.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

