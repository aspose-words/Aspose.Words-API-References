---
title: HtmlSaveOptions.document_split_heading_level property
linktitle: document_split_heading_level property
articleTitle: document_split_heading_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_heading_level property. Specifies the maximum level of headings at which to split the document"
type: docs
weight: 90
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/document_split_heading_level/
---

## HtmlSaveOptions.document_split_heading_level property

Specifies the maximum level of headings at which to split the document.
Default value is ``2``.



```python
@property
def document_split_heading_level(self) -> int:
    ...

@document_split_heading_level.setter
def document_split_heading_level(self, value: int):
    ...

```

### Remarks

When [HtmlSaveOptions.document_split_criteria](../document_split_criteria/) includes [DocumentSplitCriteria.HEADING_PARAGRAPH](../../documentsplitcriteria/#HEADING_PARAGRAPH)
and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using
**Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split.
Setting this property to zero will cause the document not to be split at heading paragraphs at all.




### Examples

Shows how to split an output HTML document by headings into several parts.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 我们使用 "Heading" 样式格式化的每个段落都可以作为标题。
# 每个标题还可能有一个标题级别，由其标题样式的数量决定。
# 以下标题的级别为 1-3。
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #1')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #2')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #3')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #4')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #5')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #6')
# 创建一个 HtmlSaveOptions 对象并将拆分标准设置为 "HeadingParagraph"。
# 这些标准将在具有 "Heading" 样式的段落处将文档拆分为多个较小的文档，
# 并将每个文档保存为本地文件系统中的单独 HTML 文件。
# 我们还将设置最大标题级别，该级别将文档拆分为 2。
# 保存文档时会在级别为 1 和 2 的标题处拆分，但不会在 3 到 9 的标题处拆分。
options = aw.saving.HtmlSaveOptions()
options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
options.document_split_heading_level = 2
# 我们的文档有四个级别为 1 - 2 的标题。其中一个标题将不会是
# 拆分点，因为它位于文档的开头。
# 保存操作将在三个位置拆分我们的文档，生成四个较小的文档。
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels.html', save_options=options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels.html')
self.assertEqual('Heading #1', doc.get_text().strip())
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels-01.html')
self.assertEqual('Heading #2\r' + 'Heading #3', doc.get_text().strip())
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels-02.html')
self.assertEqual('Heading #4', doc.get_text().strip())
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HeadingLevels-03.html')
self.assertEqual('Heading #5\r' + 'Heading #6', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.document_split_criteria](../document_split_criteria/)
* property [HtmlSaveOptions.document_part_saving_callback](../document_part_saving_callback/)

