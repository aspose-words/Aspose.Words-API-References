---
title: Orientation enumeration
linktitle: Orientation enumeration
articleTitle: Orientation enumeration
second_title: Aspose.Words for Python
description: "aspose.words.Orientation enumeration. Specifies page orientation."
type: docs
weight: 880
url: /zh/python-net/aspose.words/orientation/
---

## Orientation enumeration

Specifies page orientation.


### Members

| Name | Description |
| --- | --- |
| PORTRAIT | Portrait page orientation (narrow and tall). |
| LANDSCAPE | Landscape page orientation (wide and short). |

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 修改构建器当前节的页面设置属性并添加文本。
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# 如果我们使用文档构建器开始一个新节，
# 它将继承构建器当前的页面设置属性。
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# 我们可以使用 "ClearFormatting" 方法将其页面设置属性恢复为默认值。
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../)

