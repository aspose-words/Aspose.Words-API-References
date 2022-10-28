---
title: compare method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Document.compare method"
type: docs
weight: 540
url: /python-net/aspose.words/document/compare/
---

## compare(document, author, date_time) {#document_str_datetime}

Compares this document with another document producing changes as number of edit and format revisions [Revision](../../revision/).



```python
def compare(self, document: aspose.words.Document, author: str, date_time: datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../) |  |
| author | str |  |
| date_time | datetime |  |

The following document nodes are not compared at the moment:

* [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
  
* Item3
  
> **NOTE**
>
> Documents must not have revisions before comparison.




## compare(document, author, date_time, options) {#document_str_datetime_compareoptions}

Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../revision/).
Allows to specify comparison options using [CompareOptions](../../../aspose.words.comparing/compareoptions/).



```python
def compare(self, document: aspose.words.Document, author: str, date_time: datetime, options: aspose.words.comparing.CompareOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../) |  |
| author | str |  |
| date_time | datetime |  |
| options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) |  |

## Examples

Shows how to compare documents.

```python
doc_original = aw.Document()
builder = aw.DocumentBuilder(doc_original)
builder.writeln("This is the original document.")

doc_edited = aw.Document()
builder = aw.DocumentBuilder(doc_edited)
builder.writeln("This is the edited document.")

# Comparing documents with revisions will throw an exception.
if doc_original.revisions.count == 0 and doc_edited.revisions.count == 0:
    doc_original.compare(doc_edited, "authorName", datetime.now())

# After the comparison, the original document will gain a new revision
# for every element that is different in the edited document.
for revision in doc_original.revisions:
    print(f"Revision type: {revision.revision_type}, on a node of type \"{revision.parent_node.node_type}\"")
    print(f"\tChanged text: \"{revision.parent_node.get_text()}\"")

# Accepting these revisions will transform the original document into the edited document.
doc_original.revisions.accept_all()

self.assertEqual(doc_original.get_text(), doc_edited.get_text())
```

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
first_paragraph.paragraph_format.style = doc_edited.styles.get_by_style_identifier(aw.StyleIdentifier.HEADING1)
doc_edited.get_child(aw.NodeType.FOOTNOTE, 0, True).as_footnote().first_paragraph.runs[1].text = "Edited endnote text."
doc_edited.get_child(aw.NodeType.TABLE, 0, True).as_table().first_row.cells[1].first_paragraph.runs[0].text = "Edited Cell 2 contents"
doc_edited.get_child(aw.NodeType.SHAPE, 0, True).as_shape().first_paragraph.runs[0].text = "Edited textbox contents"
doc_edited.range.fields[0].as_field_date().use_lunar_calendar = True
doc_edited.get_child(aw.NodeType.COMMENT, 0, True).as_comment().first_paragraph.runs[0].text = "Edited comment."
doc_edited.first_section.headers_footers.header_primary.first_paragraph.runs[0].text = "Edited header contents."

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

## See Also

* module [aspose.words](../../)
* class [Document](../)

