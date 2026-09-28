---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /zh/python-net/aspose.words/pagesetup/rtl_gutter/
---

## PageSetup.rtl_gutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


```python
@property
def rtl_gutter(self) -> bool:
    ...

@rtl_gutter.setter
def rtl_gutter(self, value: bool):
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

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

