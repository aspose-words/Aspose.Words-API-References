---
title: DocumentBuilder class
linktitle: DocumentBuilder class
articleTitle: DocumentBuilder class
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder class. Provides methods to insert text, images and other content, specify font, paragraph and section formatting"
type: docs
weight: 300
url: /python-net/aspose.words/documentbuilder/
---

## DocumentBuilder class

Provides methods to insert text, images and other content, specify font, paragraph and section formatting.
To learn more, visit the [Document Builder Overview](https://docs.aspose.com/words/python-net/document-builder-overview/) documentation article.




### Remarks

[DocumentBuilder](./) makes the process of building a [Document](../document/) easier.
[Document](../document/) is a composite object consisting of a tree of nodes and while inserting content
nodes directly into the tree is possible, it requires good understanding of the tree structure.
[DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows
to insert content and formatting quickly and easily.

Create a [DocumentBuilder](./) and associate it with a [Document](../document/).

The [DocumentBuilder](./) has an internal cursor where the text will be inserted
when you call [DocumentBuilder.write()](./write/#str), [DocumentBuilder.writeln()](./writeln/#str), [DocumentBuilder.insert_break()](./insert_break/#breaktype)
and other methods. You can navigate the [DocumentBuilder](./) cursor to a different location
in a document using various MoveToXXX methods.

Use the [DocumentBuilder.font](./font/) property to specify character formatting that will apply to
all text inserted from the current position in the document onwards.

Use the [DocumentBuilder.paragraph_format](./paragraph_format/) property to specify paragraph formatting for the current
and all paragraphs that will be inserted.

Use the [DocumentBuilder.page_setup](./page_setup/) property to specify page and section properties for the current
section and all section that will be inserted.

Use the [DocumentBuilder.cell_format](./cell_format/) and [DocumentBuilder.row_format](./row_format/) properties to specify
formatting properties for table cells and rows. User the [DocumentBuilder.insert_cell()](./insert_cell/#default) and
[DocumentBuilder.end_row()](./end_row/#default) methods to build a table.

Note that [DocumentBuilder.font](./font/), [DocumentBuilder.paragraph_format](./paragraph_format/) and [DocumentBuilder.page_setup](./page_setup/) properties are updated whenever
you navigate to a different place in the document to reflect formatting properties available at the new location.




### Constructors
| Name | Description |
| --- | --- |
| [DocumentBuilder()](./__init__/#default) | Initializes a new instance of this class. |
| [DocumentBuilder(options)](./__init__/#documentbuilderoptions) | Initializes a new instance of this class. |
| [DocumentBuilder(doc)](./__init__/#document) | Initializes a new instance of this class. |
| [DocumentBuilder(doc, options)](./__init__/#document_documentbuilderoptions) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [bold](./bold/) | True if the font is formatted as bold. |
| [cell_format](./cell_format/) | Returns an object that represents current table cell formatting properties. |
| [current_node](./current_node/) | Gets the node that is currently selected in this DocumentBuilder. |
| [current_paragraph](./current_paragraph/) | Gets the paragraph that is currently selected in this [DocumentBuilder](./). |
| [current_section](./current_section/) | Gets the section that is currently selected in this [DocumentBuilder](./). |
| [current_story](./current_story/) | Gets the story that is currently selected in this [DocumentBuilder](./). |
| [current_structured_document_tag](./current_structured_document_tag/) | Gets the structured document tag that is currently selected in this [DocumentBuilder](./). |
| [document](./document/) | Gets or sets the [DocumentBuilder.document](./document/) object that this object is attached to. |
| [font](./font/) | Returns an object that represents current font formatting properties. |
| [is_at_end_of_paragraph](./is_at_end_of_paragraph/) | Returns ``True`` if the cursor is at the end of the current paragraph. |
| [is_at_end_of_structured_document_tag](./is_at_end_of_structured_document_tag/) | Returns **true** if the cursor is at the end of a structured document tag. |
| [is_at_start_of_paragraph](./is_at_start_of_paragraph/) | Returns ``True`` if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [italic](./italic/) | True if the font is formatted as italic. |
| [list_format](./list_format/) | Returns an object that represents current list formatting properties. |
| [page_setup](./page_setup/) | Returns an object that represents current page setup and section properties. |
| [paragraph_format](./paragraph_format/) | Returns an object that represents current paragraph formatting properties. |
| [row_format](./row_format/) | Returns an object that represents current table row formatting properties. |
| [underline](./underline/) | Gets/sets underline type for the current font. |

### Methods

| Name | Description |
| --- | --- |
|[ delete_row(table_index, row_index)](./delete_row/#int_int) | Deletes a row from a table. |
|[ end_bookmark(bookmark_name)](./end_bookmark/#str) | Marks the current position in the document as a bookmark end. |
|[ end_column_bookmark(bookmark_name)](./end_column_bookmark/#str) | Marks the current position in the document as a column bookmark end. The position must be in a table cell. |
|[ end_editable_range()](./end_editable_range/#default) | Marks the current position in the document as an editable range end. |
|[ end_editable_range(start)](./end_editable_range/#editablerangestart) | Marks the current position in the document as an editable range end. |
|[ end_row()](./end_row/#default) | Ends a table row in the document. |
|[ end_table()](./end_table/#default) | Ends a table in the document. |
|[ insert_break(break_type)](./insert_break/#breaktype) | Inserts a break of the specified type into the document. |
|[ insert_cell()](./insert_cell/#default) | Inserts a table cell into the document. |
|[ insert_chart(chart_type, width, height)](./insert_chart/#charttype_float_float) | Inserts an chart object into the document and scales it to the specified size. |
|[ insert_chart(chart_type, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_chart/#charttype_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts an chart object into the document and scales it to the specified size. |
|[ insert_check_box(name, checked_value, size)](./insert_check_box/#str_bool_int) | Inserts a checkbox form field at the current position. |
|[ insert_check_box(name, default_value, checked_value, size)](./insert_check_box/#str_bool_bool_int) | Inserts a checkbox form field at the current position. |
|[ insert_combo_box(name, items, selected_index)](./insert_combo_box/#str_strlist_int) | Inserts a combobox form field at the current position. |
|[ insert_document(src_doc, import_format_mode)](./insert_document/#document_importformatmode) | Inserts a document at the cursor position. |
|[ insert_document(src_doc, import_format_mode, import_format_options)](./insert_document/#document_importformatmode_importformatoptions) | Inserts a document at the cursor position. |
|[ insert_document_inline(src_doc, import_format_mode, import_format_options)](./insert_document_inline/#document_importformatmode_importformatoptions) | Inserts a document inline at the cursor position. |
|[ insert_field(field_type, update_field)](./insert_field/#fieldtype_bool) | Inserts a Word field into a document and optionally updates the field result. |
|[ insert_field(field_code)](./insert_field/#str) | Inserts a Word field into a document and updates the field result. |
|[ insert_field(field_code, field_value)](./insert_field/#str_str) | Inserts a Word field into a document without updating the field result. |
|[ insert_footnote(footnote_type, footnote_text)](./insert_footnote/#footnotetype_str) | Inserts a footnote or endnote into the document. |
|[ insert_footnote(footnote_type, footnote_text, reference_mark)](./insert_footnote/#footnotetype_str_str) | Inserts a footnote or endnote into the document. |
|[ insert_group_shape(shapes)](./insert_group_shape/#shapelist) | Groups the shapes passed as a parameter into a new GroupShape node which is inserted into the current position. |
|[ insert_group_shape(left, top, width, height, shapes)](./insert_group_shape/#float_float_float_float_shapelist) | Groups the shapes passed as a parameter into a new GroupShape node of the specified size which is inserted into the specified position. |
|[ insert_horizontal_rule()](./insert_horizontal_rule/#default) | Inserts a horizontal rule shape into the document. |
|[ insert_html(html)](./insert_html/#str) | Inserts an HTML string into the document. |
|[ insert_html(html, use_builder_formatting)](./insert_html/#str_bool) | Inserts an HTML string into the document. |
|[ insert_html(html, options)](./insert_html/#str_htmlinsertoptions) | Inserts an HTML string into the document. Allows to specify additional options. |
|[ insert_hyperlink(display_text, url_or_bookmark, is_bookmark)](./insert_hyperlink/#str_str_bool) | Inserts a hyperlink into the document. |
|[ insert_image(file_name)](./insert_image/#str) | Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale. |
|[ insert_image(stream)](./insert_image/#bytesio) | Inserts an image from a stream into the document. The image is inserted inline and at 100% scale. |
|[ insert_image(image_bytes)](./insert_image/#bytes) | Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale. |
|[ insert_image(file_name, width, height)](./insert_image/#str_float_float) | Inserts an inline image from a file or URL into the document and scales it to the specified size. |
|[ insert_image(stream, width, height)](./insert_image/#bytesio_float_float) | Inserts an inline image from a stream into the document and scales it to the specified size. |
|[ insert_image(image_bytes, width, height)](./insert_image/#bytes_float_float) | Inserts an inline image from a byte array into the document and scales it to the specified size. |
|[ insert_image(file_name, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_image/#str_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts an image from a file or URL at the specified position and size. |
|[ insert_image(stream, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_image/#bytesio_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts an image from a stream at the specified position and size. |
|[ insert_image(image_bytes, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_image/#bytes_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts an image from a byte array at the specified position and size. |
|[ insert_node(node)](./insert_node/#node) | Inserts a node before the cursor. |
|[ insert_ole_object(stream, prog_id, as_icon, presentation)](./insert_ole_object/#bytesio_str_bool_bytesio) | Inserts an embedded OLE object from a stream into the document. |
|[ insert_ole_object(file_name, is_linked, as_icon, presentation)](./insert_ole_object/#str_bool_bool_bytesio) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension. |
|[ insert_ole_object(file_name, prog_id, is_linked, as_icon, presentation)](./insert_ole_object/#str_str_bool_bool_bytesio) | Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter. |
|[ insert_ole_object_as_icon(file_name, is_linked, icon_file, icon_caption)](./insert_ole_object_as_icon/#str_bool_str_str) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension. |
|[ insert_ole_object_as_icon(file_name, prog_id, is_linked, icon_file, icon_caption)](./insert_ole_object_as_icon/#str_str_bool_str_str) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
|[ insert_ole_object_as_icon(stream, prog_id, icon_file, icon_caption)](./insert_ole_object_as_icon/#bytesio_str_str_str) | Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter. |
|[ insert_online_video(video_url, width, height)](./insert_online_video/#str_float_float) | Inserts an online video object into the document and scales it to the specified size. |
|[ insert_online_video(video_url, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_online_video/#str_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts an online video object into the document and scales it to the specified size. |
|[ insert_online_video(video_url, video_embed_code, thumbnail_image_bytes, width, height)](./insert_online_video/#str_str_bytes_float_float) | Inserts an online video object into the document and scales it to the specified size. |
|[ insert_online_video(video_url, video_embed_code, thumbnail_image_bytes, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_online_video/#str_str_bytes_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts an online video object into the document and scales it to the specified size. |
|[ insert_paragraph()](./insert_paragraph/#default) | Inserts a paragraph break into the document. |
|[ insert_shape(shape_type, width, height)](./insert_shape/#shapetype_float_float) | Inserts inline shape with specified type and size. |
|[ insert_shape(shape_type, horz_pos, left, vert_pos, top, width, height, wrap_type)](./insert_shape/#shapetype_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype) | Inserts free-floating shape with specified position, size and text wrap type. |
|[ insert_signature_line(signature_line_options)](./insert_signature_line/#signaturelineoptions) | Inserts a signature line at the current position. |
|[ insert_signature_line(signature_line_options, horz_pos, left, vert_pos, top, wrap_type)](./insert_signature_line/#signaturelineoptions_relativehorizontalposition_float_relativeverticalposition_float_wraptype) | Inserts a signature line at the specified position. |
|[ insert_structured_document_tag(type)](./insert_structured_document_tag/#sdttype) | Inserts a [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) into the document. |
|[ insert_style_separator()](./insert_style_separator/#default) | Inserts style separator into the document. |
|[ insert_table_of_contents(switches)](./insert_table_of_contents/#str) | Inserts a TOC (table of contents) field into the document. |
|[ insert_text_input(name, type, format, field_value, max_length)](./insert_text_input/#str_textformfieldtype_str_str_int) | Inserts a text form field at the current position. |
|[ move_to(node)](./move_to/#node) | Moves the cursor to an inline node or to the end of a paragraph. |
|[ move_to_bookmark(bookmark_name)](./move_to_bookmark/#str) | Moves the cursor to a bookmark. |
|[ move_to_bookmark(bookmark_name, is_start, is_after)](./move_to_bookmark/#str_bool_bool) | Moves the cursor to a bookmark with greater precision. |
|[ move_to_cell(table_index, row_index, column_index, character_index)](./move_to_cell/#int_int_int_int) | Moves the cursor to a table cell in the current section. |
|[ move_to_document_end()](./move_to_document_end/#default) | Moves the cursor to the end of the document. |
|[ move_to_document_start()](./move_to_document_start/#default) | Moves the cursor to the beginning of the document. |
|[ move_to_field(field, is_after)](./move_to_field/#field_bool) | Moves the cursor to a field in the document. |
|[ move_to_header_footer(header_footer_type)](./move_to_header_footer/#headerfootertype) | Moves the cursor to the beginning of a header or footer in the current section. |
|[ move_to_merge_field(field_name)](./move_to_merge_field/#str) | Moves the cursor to a position just beyond the specified merge field and removes the merge field. |
|[ move_to_merge_field(field_name, is_after, is_delete_field)](./move_to_merge_field/#str_bool_bool) | Moves the merge field to the specified merge field. |
|[ move_to_paragraph(paragraph_index, character_index)](./move_to_paragraph/#int_int) | Moves the cursor to a paragraph in the current section. |
|[ move_to_section(section_index)](./move_to_section/#int) | Moves the cursor to the beginning of the body in a specified section. |
|[ move_to_structured_document_tag(structured_document_tag_index, character_index)](./move_to_structured_document_tag/#int_int) | Moves the cursor to a structured document tag in the current section. |
|[ move_to_structured_document_tag(structured_document_tag, character_index)](./move_to_structured_document_tag/#structureddocumenttag_int) | Moves the cursor to the structured document tag. |
|[ pop_font()](./pop_font/#default) | Retrieves character formatting previously saved on the stack. |
|[ push_font()](./push_font/#default) | Saves current character formatting onto the stack. |
|[ start_bookmark(bookmark_name)](./start_bookmark/#str) | Marks the current position in the document as a bookmark start. |
|[ start_column_bookmark(bookmark_name)](./start_column_bookmark/#str) | Marks the current position in the document as a column bookmark start. The position must be in a table cell. |
|[ start_editable_range()](./start_editable_range/#default) | Marks the current position in the document as an editable range start. |
|[ start_table()](./start_table/#default) | Starts a table in the document. |
|[ write(text)](./write/#str) | Inserts a string into the document at the current insert position. |
|[ writeln(text)](./writeln/#str) | Inserts a string and a paragraph break into the document. |
|[ writeln()](./writeln/#default) | Inserts a paragraph break into the document. |

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Specify that we want different headers and footers for first, even and odd pages.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Create the headers, then add three pages to the document to display each header type.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Setting table formatting options for a document builder
# will apply them to every row and cell that we add with it.
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True
builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = aspose.pydrawing.Color.orange
builder.insert_cell()
builder.write('Row 1, Col 1')
builder.insert_cell()
builder.write('Row 1, Col 2')
builder.end_row()
# Changing the formatting will apply it to the current cell,
# and any new cells that we create with the builder afterward.
# This will not affect the cells that we have added previously.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Increase row height to fit the vertical text.
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 3, Col 1')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 3, Col 2')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTable.docx')
```

Shows how to use a document builder to create a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Start the table, then populate the first row with two cells.
builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
# Call the builder's "EndRow" method to start a new row.
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateTable.docx')
```

### See Also

* module [aspose.words](../)

