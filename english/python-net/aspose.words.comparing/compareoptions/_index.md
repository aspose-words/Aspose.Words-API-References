---
title: CompareOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to choose advanced options for document comparison operation."
type: docs
weight: 10
url: /python-net/aspose.words.comparing/compareoptions/
---

## CompareOptions class

Allows to choose advanced options for document comparison operation.


### Constructors
| Name | Description |
| --- | --- |
| [CompareOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [granularity](./granularity/) | Specifies whether changes are tracked by character or by word. Default value is Aspose.Words.Comparing.Granularity.WordLevel. |
| [ignore_case_changes](./ignore_case_changes/) | True indicates that documents comparison is case insensitive.  By default comparison is case sensitive. |
| [ignore_comments](./ignore_comments/) | Specifies whether to compare differences in comments.  By default comments are not ignored. |
| [ignore_dml_unique_id](./ignore_dml_unique_id/) | Specifies whether to ignore difference in DrawingML unique Id.  Default value is **false**. |
| [ignore_fields](./ignore_fields/) | Specifies whether to compare differences in fields.  By default fields are not ignored. |
| [ignore_footnotes](./ignore_footnotes/) | Specifies whether to compare differences in footnotes and endnotes.  By default footnotes are not ignored. |
| [ignore_formatting](./ignore_formatting/) | True indicates that formatting is ignored.  By default document formatting is not ignored. |
| [ignore_headers_and_footers](./ignore_headers_and_footers/) | True indicates that headers and footers content is ignored.  By default headers and footers are not ignored. |
| [ignore_tables](./ignore_tables/) | Specifies whether to compare the differences in data contained in tables.  By default tables are not ignored. |
| [ignore_textboxes](./ignore_textboxes/) | Specifies whether to compare differences in the data contained within text boxes.  By default textboxes are not ignored. |
| [target](./target/) | Specifies which document shall be used as a target during comparison. |

### Examples

Shows how to filter specific types of document elements when making a comparison.

```python
# Create the original document and populate it with various kinds of elements.
doc_original = aw.Document()
builder = aw.DocumentBuilder(doc_original)

# Paragraph text referenced with an endnote:
builder.writeln("Hello world! This is the first paragraph.")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Original endnote text.")

# Table:
builder.start_table()
builder.insert_cell()
builder.write("Original cell 1 text")
builder.insert_cell()
builder.write("Original cell 2 text")
builder.end_table()

# Textbox:
text_box = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 150, 20)
builder.move_to(text_box.first_paragraph)
builder.write("Original textbox contents")

# DATE field:
builder.move_to(doc_original.first_section.body.append_paragraph(""))
builder.insert_field(" DATE ")

# Comment:
new_comment = aw.Comment(doc_original, "John Doe", "J.D.", datetime.now())
new_comment.set_text("Original comment.")
builder.current_paragraph.append_child(new_comment)

# Header:
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln("Original header contents.")

# Create a clone of our document and perform a quick edit on each of the cloned document's elements.
doc_edited = doc_original.clone(True).as_document()
first_paragraph = doc_edited.first_section.body.first_paragraph

first_paragraph.runs[0].text = "hello world! this is the first paragraph, after editing."
first_paragraph.paragraph_format.style = doc_edited.styles[aw.StyleIdentifier.HEADING1]
doc_edited.get_child(aw.NodeType.FOOTNOTE, 0, True).as_footnote().first_paragraph.runs[1].text = "Edited endnote text."
doc_edited.get_child(aw.NodeType.TABLE, 0, True).as_table().first_row.cells[1].first_paragraph.runs[0].text = "Edited Cell 2 contents"
doc_edited.get_child(aw.NodeType.SHAPE, 0, True).as_shape().first_paragraph.runs[0].text = "Edited textbox contents"
doc_edited.range.fields[0].as_field_date().use_lunar_calendar = True
doc_edited.get_child(aw.NodeType.COMMENT, 0, True).as_comment().first_paragraph.runs[0].text = "Edited comment."
doc_edited.first_section.headers_footers[aw.HeaderFooterType.HEADER_PRIMARY].first_paragraph.runs[0].text = "Edited header contents."

# Comparing documents creates a revision for every edit in the edited document.
# A CompareOptions object has a series of flags that can suppress revisions
# on each respective type of element, effectively ignoring their change.
compare_options = aw.comparing.CompareOptions()
compare_options.ignore_formatting = False
compare_options.ignore_case_changes = False
compare_options.ignore_comments = False
compare_options.ignore_tables = False
compare_options.ignore_fields = False
compare_options.ignore_footnotes = False
compare_options.ignore_textboxes = False
compare_options.ignore_headers_and_footers = False
compare_options.target = aw.comparing.ComparisonTargetType.NEW

doc_original.compare(doc_edited, "John Doe", datetime.now(), compare_options)
doc_original.save(ARTIFACTS_DIR + "Document.compare_options.docx")
```

### See Also

* module [aspose.words.comparing](../)

