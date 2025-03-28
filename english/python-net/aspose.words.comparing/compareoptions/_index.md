﻿---
title: CompareOptions class
linktitle: CompareOptions class
articleTitle: CompareOptions class
second_title: Aspose.Words for Python
description: "aspose.words.comparing.CompareOptions class. Allows to choose additional options for document comparison operation"
type: docs
weight: 20
url: /python-net/aspose.words.comparing/compareoptions/
---

## CompareOptions class

Allows to choose additional options for document comparison operation.
To learn more, visit the [Compare Documents](https://docs.aspose.com/words/python-net/compare-documents/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [CompareOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [advanced_options](./advanced_options/) | Specifies advanced compare options that might help to produce more precise comparison output. |
| [compare_moves](./compare_moves/) | Specifies whether to compare differences   between the two documents. |
| [granularity](./granularity/) | Specifies whether changes are tracked by character or by word. |
| [ignore_case_changes](./ignore_case_changes/) | True indicates that documents comparison is case insensitive. |
| [ignore_comments](./ignore_comments/) | Specifies whether to compare differences in comments. |
| [ignore_dml_unique_id](./ignore_dml_unique_id/) | Specifies whether to ignore difference in DrawingML unique Id. |
| [ignore_fields](./ignore_fields/) | Specifies whether to compare differences in fields. |
| [ignore_footnotes](./ignore_footnotes/) | Specifies whether to compare differences in footnotes and endnotes. |
| [ignore_formatting](./ignore_formatting/) | True indicates that formatting is ignored. |
| [ignore_headers_and_footers](./ignore_headers_and_footers/) | True indicates that headers and footers content is ignored. |
| [ignore_tables](./ignore_tables/) | Specifies whether to compare the differences in data contained in tables. |
| [ignore_textboxes](./ignore_textboxes/) | Specifies whether to compare differences in the data contained within text boxes. |
| [target](./target/) | Specifies which document shall be used as a target during comparison. |

### Examples

Shows how to filter specific types of document elements when making a comparison.

```python
# Create the original document and populate it with various kinds of elements.
doc_original = aw.Document()
builder = aw.DocumentBuilder(doc=doc_original)
# Paragraph text referenced with an endnote:
builder.writeln('Hello world! This is the first paragraph.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Original endnote text.')
# Table:
builder.start_table()
builder.insert_cell()
builder.write('Original cell 1 text')
builder.insert_cell()
builder.write('Original cell 2 text')
builder.end_table()
# Textbox:
text_box = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=20)
builder.move_to(text_box.first_paragraph)
builder.write('Original textbox contents')
# DATE field:
builder.move_to(doc_original.first_section.body.append_paragraph(''))
builder.insert_field(field_code=' DATE ')
# Comment:
new_comment = aw.Comment(doc=doc_original, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
new_comment.set_text('Original comment.')
builder.current_paragraph.append_child(new_comment)
# Header:
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Original header contents.')
# Create a clone of our document and perform a quick edit on each of the cloned document's elements.
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
# Comparing documents creates a revision for every edit in the edited document.
# A CompareOptions object has a series of flags that can suppress revisions
# on each respective type of element, effectively ignoring their change.
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

* module [aspose.words.comparing](../)

