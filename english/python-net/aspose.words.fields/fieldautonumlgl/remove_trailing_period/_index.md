---
title: FieldAutoNumLgl.remove_trailing_period property
linktitle: remove_trailing_period property
articleTitle: remove_trailing_period property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.remove_trailing_period property. Gets or sets whether to display the number without a trailing period."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldautonumlgl/remove_trailing_period/
---

## FieldAutoNumLgl.remove_trailing_period property

Gets or sets whether to display the number without a trailing period.


### Examples

Shows how to organize a document using AUTONUMLGL fields.

```python
def test_field_auto_num_lgl(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    filler_text = (
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
        "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ")

    # AUTONUMLGL fields display a number that increments at each AUTONUMLGL field within its current heading level.
    # These fields maintain a separate count for each heading level,
    # and each field also displays the AUTONUMLGL field counts for all heading levels below its own.
    # Changing the count for any heading level resets the counts for all levels above that level to 1.
    # This allows us to organize our document in the form of an outline list.
    # This is the first AUTONUMLGL field at a heading level of 1, displaying "1." in the document.
    ExField._insert_numbered_clause(builder, "\tHeading 1", filler_text, aw.StyleIdentifier.HEADING1)

    # This is the second AUTONUMLGL field at a heading level of 1, so it will display "2.".
    ExField._insert_numbered_clause(builder, "\tHeading 2", filler_text, aw.StyleIdentifier.HEADING1)

    # This is the first AUTONUMLGL field at a heading level of 2,
    # and the AUTONUMLGL count for the heading level below it is "2", so it will display "2.1.".
    ExField._insert_numbered_clause(builder, "\tHeading 3", filler_text, aw.StyleIdentifier.HEADING2)

    # This is the first AUTONUMLGL field at a heading level of 3.
    # Working in the same way as the field above, it will display "2.1.1.".
    ExField._insert_numbered_clause(builder, "\tHeading 4", filler_text, aw.StyleIdentifier.HEADING3)

    # This field is at a heading level of 2, and its respective AUTONUMLGL count is at 2, so the field will display "2.2.".
    ExField._insert_numbered_clause(builder, "\tHeading 5", filler_text, aw.StyleIdentifier.HEADING2)

    # Incrementing the AUTONUMLGL count for a heading level below this one
    # has reset the count for this level so that this field will display "2.2.1.".
    ExField._insert_numbered_clause(builder, "\tHeading 6", filler_text, aw.StyleIdentifier.HEADING3)

    for field in doc.range.fields:
        if field.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL:
            field = field.as_field_auto_num_lgl()
            # The separator character, which appears in the field result immediately after the number,
            # is a full stop by default. If we leave this property null,
            # our last AUTONUMLGL field will display "2.2.1." in the document.
            self.assertIsNone(field.separator_character)

            # Setting a custom separator character and removing the trailing period
            # will change that field's appearance from "2.2.1." to "2:2:1".
            # We will apply this to all the fields that we have created.
            field.separator_character = ":"
            field.remove_trailing_period = True
            self.assertEqual(" AUTONUMLGL  \\s : \\e", field.get_field_code())

    doc.save(ARTIFACTS_DIR + "Field.field_auto_num_lgl.docx")

@staticmethod
def _insert_numbered_clause(builder: aw.DocumentBuilder, heading: str, contents: str, heading_style: aw.StyleIdentifier):
    """Uses a document builder to insert a clause numbered by an AUTONUMLGL field."""

    builder.insert_field(aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)

    # This text will belong to the auto num legal field above it.
    # It will collapse when we click the arrow next to the corresponding AUTONUMLGL field in Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

