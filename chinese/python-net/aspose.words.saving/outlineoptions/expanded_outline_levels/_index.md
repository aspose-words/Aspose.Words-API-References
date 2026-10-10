---
title: OutlineOptions.expanded_outline_levels property
linktitle: expanded_outline_levels property
articleTitle: expanded_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.expanded_outline_levels property. Specifies how many levels in the document outline to show expanded when the file is viewed."
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/outlineoptions/expanded_outline_levels/
---

## OutlineOptions.expanded_outline_levels property

Specifies how many levels in the document outline to show expanded when the file is viewed.


```python
@property
def expanded_outline_levels(self) -> int:
    ...

@expanded_outline_levels.setter
def expanded_outline_levels(self, value: int):
    ...

```

### Remarks

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items
in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入 1 到 5 级的标题。
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 输出的 PDF 文档将包含大纲，即列出文档正文中标题的目录。
# 单击此大纲中的条目将跳转到相应标题的位置。
# 将 "HeadingsOutlineLevels" 属性设置为 "4"，以从大纲中排除所有级别高于 4 的标题。
options.outline_options.headings_outline_levels = 4
# 如果大纲条目在自身与下一个相同或更低级别的条目之间有更高级别的后续条目，
# 该条目左侧会出现一个箭头。此条目是多个此类 "sub-entries" 的 "owner"。
# 在我们的文档中，来自第 5 级标题的大纲条目是第二个第 4 级大纲条目的子条目，
# 第4和第5级标题条目是第二个第3级条目的子条目，依此类推。
# 在大纲中，我们可以点击 "owner" 条目的箭头来折叠/展开其所有子条目。
# 将 "ExpandedOutlineLevels" 属性设置为 "2"，以自动展开所有第2级及以下的标题大纲条目
# 并在打开文档时折叠所有第3级及以上的条目。
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

