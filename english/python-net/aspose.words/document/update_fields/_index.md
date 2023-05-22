---
title: Document.update_fields method
linktitle: update_fields method
articleTitle: update_fields method
second_title: Aspose.Words for Python
description: "Document.update_fields method. Updates the values of fields in the whole document."
type: docs
weight: 720
url: /python-net/aspose.words/document/update_fields/
---

## update_fields() {#default}

Updates the values of fields in the whole document.


```python
def update_fields(self):
    ...
```

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact.
Therefore, you would usually want to call this method before saving if you have modified the document
programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update
and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF).
The page layout-related fields are updated when you render a document or call [Document.update_page_layout()](../update_page_layout/#default).

Use the [Document.normalize_field_types()](../normalize_field_types/#default) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.update_fields()](../../range/update_fields/#default).




### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a table of contents for the first page of the document.
# Configure the table to pick up paragraphs with headings of levels 1 to 3.
# Also, set its entries to be hyperlinks that will take us
# to the location of the heading when left-clicked in Microsoft Word.
builder.insert_table_of_contents("\\o \"1-3\" \\h \\z \\u")
builder.insert_break(aw.BreakType.PAGE_BREAK)

# Populate the table of contents by adding paragraphs with heading styles.
# Each such heading with a level between 1 and 3 will create an entry in the table.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln("Heading 1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln("Heading 1.1")
builder.writeln("Heading 1.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln("Heading 2")
builder.writeln("Heading 3")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln("Heading 3.1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln("Heading 3.1.1")
builder.writeln("Heading 3.1.2")
builder.writeln("Heading 3.1.3")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln("Heading 3.1.3.1")
builder.writeln("Heading 3.1.3.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln("Heading 3.2")
builder.writeln("Heading 3.3")

# A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc.update_fields()
doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_toc.docx")
```

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a QUOTE field, which will display the value of its Text property.
field = builder.insert_field(aw.fields.FieldType.FIELD_QUOTE, True).as_field_quote()
field.text = "\"Quoted text\""

self.assertEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.get_field_code())

# Insert a QUOTE field and nest a DATE field inside it.
# DATE fields update their value to the current date every time we open the document using Microsoft Word.
# Nesting the DATE field inside the QUOTE field like this will freeze its value
# to the date when we created the document.
builder.write("\nDocument creation date: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_QUOTE, True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(aw.fields.FieldType.FIELD_DATE, True)

today = datetime.now().strftime("%d/%m/%Y").lstrip('0')

self.assertEqual(" QUOTE \u0013 DATE \u0014" + today + "\u0015", field.get_field_code())

# Update all the fields to display their correct results.
doc.update_fields()

self.assertEqual("\"Quoted text\"", doc.range.fields[0].result)

doc.save(ARTIFACTS_DIR + "Field.field_quote.docx")
```

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a UserInformation object and set it as the data source for fields that display user information.
user_information = aw.fields.UserInformation()
user_information.name = "John Doe"
user_information.initials = "J. D."
user_information.address = "123 Main Street"

doc.field_options.current_user = user_information

# Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
# the respective properties of the UserInformation object that we have created above.
self.assertEqual(user_information.name, builder.insert_field(" USERNAME ").result)
self.assertEqual(user_information.initials, builder.insert_field(" USERINITIALS ").result)
self.assertEqual(user_information.address, builder.insert_field(" USERADDRESS ").result)

# The field options object also has a static default user that fields from all documents can refer to.
user_information.default_user.name = "Default User"
user_information.default_user.initials = "D. U."
user_information.default_user.address = "One Microsoft Way"
doc.field_options.current_user = aw.fields.UserInformation.default_user

self.assertEqual("Default User", builder.insert_field(" USERNAME ").result)
self.assertEqual("D. U.", builder.insert_field(" USERINITIALS ").result)
self.assertEqual("One Microsoft Way", builder.insert_field(" USERADDRESS ").result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "FieldOptions.current_user.docx")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

