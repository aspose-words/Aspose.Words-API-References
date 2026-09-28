---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
---

## OutlineOptions.create_outlines_for_headings_in_tables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```python
@property
def create_outlines_for_headings_in_tables(self) -> bool:
    ...

@create_outlines_for_headings_in_tables.setter
def create_outlines_for_headings_in_tables(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个包含三行的表格。第一行，
# 其文本将以标题样式格式化，作为列标题。
builder.start_table()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('Customers')
builder.end_row()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.write('John Doe')
builder.end_row()
builder.insert_cell()
builder.write('Jane Doe')
builder.end_table()
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
pdf_save_options = aw.saving.PdfSaveOptions()
# 输出的 PDF 文档将包含大纲，即列出文档正文中标题的目录。
# 单击此大纲中的条目将跳转到相应标题的位置。
# 将 "HeadingsOutlineLevels" 属性设置为 "1"，以获取大纲
# 仅注册标题级别不大于 1 的标题。
pdf_save_options.outline_options.headings_outline_levels = 1
# 将 "CreateOutlinesForHeadingsInTables" 属性设置为 "false"，以排除表格中的所有标题，
# 例如我们上面从大纲中创建的那个。
# 将 "CreateOutlinesForHeadingsInTables" 属性设置为 "true"，以包含表格中的所有标题
# 在大纲中，前提是它们的标题级别不大于 "HeadingsOutlineLevels" 属性的值。
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

