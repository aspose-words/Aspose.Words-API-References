---
title: SdtType enumeration
linktitle: SdtType enumeration
articleTitle: SdtType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.markup.SdtType enumeration. Specifies the type of a structured document tag (SDT) node."
type: docs
weight: 150
url: /python-net/aspose.words.markup/sdttype/
---

## SdtType enumeration

Specifies the type of a structured document tag (SDT) node.


### Members

| Name | Description |
| --- | --- |
| NONE | No type is assigned to the SDT. |
| BIBLIOGRAPHY | The SDT represents a bibliography entry. |
| CITATION | The SDT represents a citation. |
| EQUATION | The SDT represents an equation. |
| DROP_DOWN_LIST | The SDT represents a drop down list when displayed in the document. |
| COMBO_BOX | The SDT represents a combo box when displayed in the document. |
| DATE | The SDT represents a date picker when displayed in the document. |
| BUILDING_BLOCK_GALLERY | The SDT represents a building block gallery type. |
| DOC_PART_OBJ | The SDT represents a document part type. |
| GROUP | The SDT represents a restricted grouping when displayed in the document. |
| PICTURE | The SDT represents a picture when displayed in the document. |
| RICH_TEXT | The SDT represents a rich text box when displayed in the document. |
| PLAIN_TEXT | The SDT represents a plain text box when displayed in the document. |
| CHECKBOX | The SDT represents a checkbox when displayed in the document. |
| REPEATING_SECTION | The SDT represents repeating section type when displayed in the document. |
| REPEATING_SECTION_ITEM | The SDT represents repeating section item. |
| ENTITY_PICKER | The SDT represents an entity picker that allows the user to select an instance of an external content type. |

### Examples

Shows how to work with styles for content control elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two ways to apply a style from the document to a structured document tag.
# 1 -  Apply a style object from the document's style collection:
quote_style = doc.styles.get_by_style_identifier(aw.StyleIdentifier.QUOTE)
sdt_plain_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_plain_text.style = quote_style

# 2 -  Reference a style in the document by name:
sdt_rich_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.RICH_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_rich_text.style_name = "Quote"

builder.insert_node(sdt_plain_text)
builder.insert_node(sdt_rich_text)

self.assertEqual(aw.NodeType.STRUCTURED_DOCUMENT_TAG, sdt_plain_text.node_type)

tags = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)

for node in tags:
    sdt = node.as_structured_document_tag()
    print(sdt.word_open_xml_minimal)
    self.assertEqual(aw.StyleIdentifier.QUOTE, sdt.style.style_identifier)
    self.assertEqual("Quote", sdt.style_name)
```

Shows how to fill a table with data from in an XML part.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

xml_part = doc.custom_xml_parts.add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>")

# Create headers for data from the XML content.
table = builder.start_table()
builder.insert_cell()
builder.write("Title")
builder.insert_cell()
builder.write("Author")
builder.end_row()
builder.end_table()

# Create a table with a repeating section inside.
repeating_section_sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.REPEATING_SECTION, aw.markup.MarkupLevel.ROW)
repeating_section_sdt.xml_mapping.set_mapping(xml_part, "/books[1]/book", "")
table.append_child(repeating_section_sdt)

# Add repeating section item inside the repeating section and mark it as a row.
# This table will have a row for each element that we can find in the XML document
# using the "/books[1]/book" XPath, of which there are three.
repeating_section_item_sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.REPEATING_SECTION_ITEM, aw.markup.MarkupLevel.ROW)
repeating_section_sdt.append_child(repeating_section_item_sdt)

row = aw.tables.Row(doc)
repeating_section_item_sdt.append_child(row)

# Map XML data with created table cells for the title and author of each book.
title_sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.CELL)
title_sdt.xml_mapping.set_mapping(xml_part, "/books[1]/book[1]/title[1]", "")
row.append_child(title_sdt)

author_sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.CELL)
author_sdt.xml_mapping.set_mapping(xml_part, "/books[1]/book[1]/author[1]", "")
row.append_child(author_sdt)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.fill_table_using_repeating_section_item.docx")
```

Shows how to create group structured document tag at the Row level.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()

# Create a Group structured document tag at the Row level.
group_sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.GROUP, aw.markup.MarkupLevel.ROW)
table.append_child(group_sdt)
group_sdt.is_showing_placeholder_text = False
group_sdt.remove_all_children()

# Create a child row of the structured document tag.
row = aw.tables.Row(doc)
group_sdt.append_child(row)

cell = aw.tables.Cell(doc)
row.append_child(cell)

builder.end_table()

# Insert cell contents.
cell.ensure_minimum()
builder.move_to(cell.last_paragraph)
builder.write("Lorem ipsum dolor.")

# Insert text after the table.
builder.move_to(table.next_sibling)
builder.write("Nulla blandit nisi.")

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.SdtAtRowLevel.docx")
```

Shows how to create a structured document tag of the Citation type.

```python
doc = aw.Document()

sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CITATION, aw.markup.MarkupLevel.INLINE)
paragraph = doc.first_section.body.first_paragraph
paragraph.append_child(sdt)

# Create a Citation field.
builder = aw.DocumentBuilder(doc)
builder.move_to_paragraph(0, -1)
builder.insert_field(r"CITATION Ath22 \l 1033 ", "(John Lennon, 2022)")

# Move the field to the structured document tag.
while (sdt.next_sibling is not None):
    sdt.append_child(sdt.next_sibling)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.Citation.docx")
```

### See Also

* module [aspose.words.markup](../)

