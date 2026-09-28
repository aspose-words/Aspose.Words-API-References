---
title: PageSetup.multiple_pages property
linktitle: multiple_pages property
articleTitle: multiple_pages property
second_title: Aspose.Words for Python
description: "PageSetup.multiple_pages property. For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet."
type: docs
weight: 270
url: /zh/python-net/aspose.words/pagesetup/multiple_pages/
---

## PageSetup.multiple_pages property

For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.


```python
@property
def multiple_pages(self) -> aspose.words.settings.MultiplePagesType:
    ...

@multiple_pages.setter
def multiple_pages(self, value: aspose.words.settings.MultiplePagesType):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# 插入跨越多页的文本。
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# 装订线在左侧或右侧页面边距添加空白，
# 以弥补书籍中心折叠导致的页面布局被侵占。
page_setup = doc.sections[0].page_setup
# 确定页面在边距内可用于文本的空间量，然后添加一定量以填充边距。
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# 将 "RtlGutter" 属性设置为 "true"，以在从右到左的文本中将装订线放置在更合适的位置。
page_setup.rtl_gutter = True
# 将 "MultiplePages" 属性设置为 "MultiplePagesType.MirrorMargins" 以交替
# 每页左右页面边距的位置。
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

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

