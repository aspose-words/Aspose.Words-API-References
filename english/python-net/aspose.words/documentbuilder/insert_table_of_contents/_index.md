---
title: DocumentBuilder.insert_table_of_contents method
linktitle: insert_table_of_contents method
articleTitle: insert_table_of_contents method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_table_of_contents method. Inserts a TOC (table of contents) field into the document."
type: docs
weight: 500
url: /python-net/aspose.words/documentbuilder/insert_table_of_contents/
---

## insert_table_of_contents(switches) {#str}

Inserts a TOC (table of contents) field into the document.


```python
def insert_table_of_contents(self, switches: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| switches | str | The TOC field switches. |

### Remarks

This method inserts a TOC (table of contents) field into the document at
the current position.

A table of contents in a Word document can be built in a number of ways
and formatted using a variety of options. The way the table is built and
displayed by Microsoft Word is controlled by the field switches.

The easiest way to specify the switches is to insert and configure a table of
contents into a Word document using the Insert-\>Reference-\>Index and Tables menu,
then switch display of field codes on to see the switches. You can press Alt+F9 in
Microsoft Word to toggle display of field codes on or off.

For example, after creating a table of contents, the following field is inserted
into the document: **{ TOC \\o "1-3" \\h \\z \\u }**.
You can copy **\\o "1-3" \\h \\z \\u** and use it as the switches parameter.

Note that [DocumentBuilder.insert_table_of_contents()](./#str) will only insert a TOC field, but
will not actually build the table of contents. The table of contents is built by
Microsoft Word when the field is updated.

If you insert a table of contents using this method and then open the file
in Microsoft Word, you will not see the table of contents because the TOC field
has not yet been updated.

In Microsoft Word, fields are not automatically updated when a document is opened,
but you can update fields in a document at any time by pressing F9.




### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a table of contents for the first page of the document.
# Configure the table to pick up paragraphs with headings of levels 1 to 3.
# Also, set its entries to be hyperlinks that will take us
# to the location of the heading when left-clicked in Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Populate the table of contents by adding paragraphs with heading styles.
# Each such heading with a level between 1 and 3 will create an entry in the table.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

