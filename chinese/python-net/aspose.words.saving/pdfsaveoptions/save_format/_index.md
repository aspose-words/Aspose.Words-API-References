---
title: PdfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 320
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/save_format/
---

## PdfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.PDF](../../../aspose.words/saveformat/#PDF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

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

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

