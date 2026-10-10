---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 260
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/outline_options/
---

## PdfSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outline_options](./) class.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

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
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# 输出的 PDF 文档将包含大纲，即列出文档正文中标题的目录。
# 单击此大纲中的条目将跳转到相应标题的位置。
# 将 "HeadingsOutlineLevels" 属性设置为 "2"，以从大纲中排除所有级别高于 2 的标题。
# 我们上面插入的最后两个标题将不会出现。
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

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
* class [PdfSaveOptions](../)

