---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入可作为目录条目的 1 级和 5 级标题。
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.PdfSaveOptions()
# 输出的 PDF 文档将包含大纲，即列出文档正文中标题的目录。
# 单击此大纲中的条目将跳转到相应标题的位置。
# 将 "HeadingsOutlineLevels" 属性设置为 "5"，以在大纲中包含所有 5 级及以下的标题。
save_options.outline_options.headings_outline_levels = 5
# 此文档包含 1 级和 5 级标题，且没有 2、3、4 级标题。
# 输出的 PDF 文档将把大纲的 2、3、4 级视为 "missing"（缺失）。
# 将 "CreateMissingOutlineLevels" 属性设置为 "true"，以在大纲中包含所有缺失的级别，
# 由于没有可用的标题，留下空白的大纲条目。
# 将 "CreateMissingOutlineLevels" 属性设置为 "false"，以忽略缺失的大纲级别，
# 并将大纲的 5 级标题视为 2 级。
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

