---
title: PageSetup.sheets_per_booklet property
linktitle: sheets_per_booklet property
articleTitle: sheets_per_booklet property
second_title: Aspose.Words for Python
description: "PageSetup.sheets_per_booklet property. Returns or sets the number of pages to be included in each booklet."
type: docs
weight: 400
url: /zh/python-net/aspose.words/pagesetup/sheets_per_booklet/
---

## PageSetup.sheets_per_booklet property

Returns or sets the number of pages to be included in each booklet.


```python
@property
def sheets_per_booklet(self) -> int:
    ...

@sheets_per_booklet.setter
def sheets_per_booklet(self, value: int):
    ...

```

### Examples

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# 插入跨越 16 页的文本。
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# 将第一节的 "PageSetup" 属性配置为以书折形式打印文档。
# 当我们双面打印此文档时，可以取出页面并将其堆叠
# 并一次性在中间对折。文档内容将排列成书折。
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# 我们只能以 4 的倍数指定纸张数量。
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

