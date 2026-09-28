---
title: CompareOptions.ignore_textboxes property
linktitle: ignore_textboxes property
articleTitle: ignore_textboxes property
second_title: Aspose.Words for Python
description: "CompareOptions.ignore_textboxes property. Specifies whether to compare differences in the data contained within text boxes."
type: docs
weight: 130
url: /zh/python-net/aspose.words.comparing/compareoptions/ignore_textboxes/
---

## CompareOptions.ignore_textboxes property

Specifies whether to compare differences in the data contained within text boxes.


```python
@property
def ignore_textboxes(self) -> bool:
    ...

@ignore_textboxes.setter
def ignore_textboxes(self, value: bool):
    ...

```

### Remarks

By default, textboxes are not ignored.


### Examples

Shows how to filter specific types of document elements when making a comparison.

```python
# 创建原始文档并填充各种元素。
doc_original = aw.Document()
builder = aw.DocumentBuilder(doc=doc_original)
# 段落文本引用了脚注：
builder.writeln('Hello world! This is the first paragraph.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Original endnote text.')
# 表格：
builder.start_table()
builder.insert_cell()
builder.write('Original cell 1 text')
builder.insert_cell()
builder.write('Original cell 2 text')
builder.end_table()
# 文本框：
text_box = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=20)
builder.move_to(text_box.first_paragraph)
builder.write('Original textbox contents')
# 日期字段：
builder.move_to(doc_original.first_section.body.append_paragraph(''))
builder.insert_field(field_code=' DATE ')
# 注释：
new_comment = aw.Comment(doc=doc_original, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
new_comment.set_text('Original comment.')
builder.current_paragraph.append_child(new_comment)
# 页眉：
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Original header contents.')
# 创建文档的克隆并对每个克隆文档的元素进行快速编辑。
doc_edited = doc_original.clone(True).as_document()
first_paragraph = doc_edited.first_section.body.first_paragraph
first_paragraph.runs[0].text = 'hello world! this is the first paragraph, after editing.'
first_paragraph.paragraph_format.style = doc_edited.styles.get_by_style_identifier(aw.StyleIdentifier.HEADING1)
doc_edited.get_child(aw.NodeType.FOOTNOTE, 0, True).as_footnote().first_paragraph.runs[1].text = 'Edited endnote text.'
doc_edited.get_child(aw.NodeType.TABLE, 0, True).as_table().first_row.cells[1].first_paragraph.runs[0].text = 'Edited Cell 2 contents'
doc_edited.get_child(aw.NodeType.SHAPE, 0, True).as_shape().first_paragraph.runs[0].text = 'Edited textbox contents'
doc_edited.range.fields[0].as_field_date().use_lunar_calendar = True
doc_edited.get_child(aw.NodeType.COMMENT, 0, True).as_comment().first_paragraph.runs[0].text = 'Edited comment.'
doc_edited.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).first_paragraph.runs[0].text = 'Edited header contents.'
# 比较文档会为已编辑文档中的每一次编辑创建一个修订。
# CompareOptions 对象具有一系列可以抑制修订的标志
# 针对每种相应类型的元素，有效地忽略它们的更改。
compare_options = aw.comparing.CompareOptions()
compare_options.compare_moves = False
compare_options.ignore_formatting = False
compare_options.ignore_case_changes = False
compare_options.ignore_comments = False
compare_options.ignore_tables = False
compare_options.ignore_fields = False
compare_options.ignore_footnotes = False
compare_options.ignore_textboxes = False
compare_options.ignore_headers_and_footers = False
compare_options.target = aw.comparing.ComparisonTargetType.NEW
doc_original.compare(document=doc_edited, author='John Doe', date_time=datetime.datetime.now(), options=compare_options)
doc_original.save(file_name=ARTIFACTS_DIR + 'Revision.CompareOptions.docx')
```

### See Also

* module [aspose.words.comparing](../../)
* class [CompareOptions](../)

