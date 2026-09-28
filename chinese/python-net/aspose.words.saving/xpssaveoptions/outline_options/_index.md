---
title: XpsSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/xpssaveoptions/outline_options/
---

## XpsSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Note that [OutlineOptions.expanded_outline_levels](../../outlineoptions/expanded_outline_levels/) option will not work when saving to XPS.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入可作为目录条目（TOC）的标题，级别分别为 1、2 和 3。
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# 创建一个 "XpsSaveOptions" 对象，以便我们可以将其传递给文档的 "Save" 方法
# 以修改该方法将文档转换为 .XPS 的方式。
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# 输出的 XPS 文档将包含大纲，即列出文档正文中标题的目录。
# 单击此大纲中的条目将跳转到相应标题的位置。
# 将 "HeadingsOutlineLevels" 属性设置为 "2"，以从大纲中排除所有级别高于 2 的标题。
# 我们上面插入的最后两个标题将不会出现。
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

