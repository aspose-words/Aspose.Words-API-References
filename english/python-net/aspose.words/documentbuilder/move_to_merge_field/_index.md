---
title: move_to_merge_field method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.DocumentBuilder.move_to_merge_field method"
type: docs
weight: 550
url: /python-net/aspose.words/documentbuilder/move_to_merge_field/
---

## move_to_merge_field(field_name) {#str}

Moves the cursor to a position just beyond the specified merge field and removes the merge field.


```python
def move_to_merge_field(self, field_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_name | str |  |

Note that this method deletes the merge field from the document after moving the cursor.




### Returns

``True`` if the merge field was found and the cursor was moved; ``False`` otherwise.


## move_to_merge_field(field_name, is_after, is_delete_field) {#str_bool_bool}

Moves the merge field to the specified merge field.


```python
def move_to_merge_field(self, field_name: str, is_after: bool, is_delete_field: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_name | str |  |
| is_after | bool |  |
| is_delete_field | bool |  |

### Returns

``True`` if the merge field was found and the cursor was moved; ``False`` otherwise.


## Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
# and then fill them manually.
builder.insert_field(" MERGEFIELD Chairman ")
builder.insert_field(" MERGEFIELD ChiefFinancialOfficer ")
builder.insert_field(" MERGEFIELD ChiefTechnologyOfficer ")

builder.move_to_merge_field("Chairman")
builder.bold = True
builder.writeln("John Doe")

builder.move_to_merge_field("ChiefFinancialOfficer")
builder.italic = True
builder.writeln("Jane Doe")

builder.move_to_merge_field("ChiefTechnologyOfficer")
builder.italic = True
builder.writeln("John Bloggs")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.fill_merge_fields.docx")
```

Shows how to insert checkbox form fields into MERGEFIELDs as merge data during mail merge.

```python
def test_insert_check_box(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Use MERGEFIELDs with "TableStart"/"TableEnd" tags to define a mail merge region
    # which belongs to a data source named "StudentCourse" and has a MERGEFIELD which accepts data from a column named "CourseName".
    builder.start_table()
    builder.insert_cell()
    builder.insert_field(" MERGEFIELD  TableStart:StudentCourse ")
    builder.insert_cell()
    builder.insert_field(" MERGEFIELD  CourseName ")
    builder.insert_cell()
    builder.insert_field(" MERGEFIELD  TableEnd:StudentCourse ")
    builder.end_table()

    doc.mail_merge.field_merging_callback = ExMailMergeEvent.HandleMergeFieldInsertCheckBox()

    data_table = ExMailMergeEvent.get_student_course_data_table()

    doc.mail_merge.execute_with_regions(data_table)
    doc.save(ARTIFACTS_DIR + "MailMergeEvent.insert_check_box.docx")

class HandleMergeFieldInsertCheckBox(aw.mailmerging.IFieldMergingCallback):
    """Upon encountering a MERGEFIELD with a specific name, inserts a check box form field instead of merge data text."""

    def __init__(self):
        self.check_box_count = 0

    def field_merging(self, args: aw.mailmerging.FieldMergingArgs):
        """Called when a mail merge merges data into a MERGEFIELD."""

        if args.document_field_name == "CourseName":
            self.assertEqual("StudentCourse", args.table_name)

            builder = aw.DocumentBuilder(args.document)
            builder.move_to_merge_field(args.field_name)
            builder.insert_check_box(args.document_field_name + self.check_box_count, False, 0)

            field_value = args.field_value.to_string()

            # In this case, for every record index 'n', the corresponding field value is "Course n".
            self.assertEqual(ord(field_value[7]), args.record_index)

            builder.write(field_value)
            self.check_box_count += 1

    def image_field_merging(self, args: aw.mailmerging.ImageFieldMergingArgs):

        # Do nothing.
        pass

@staticmethod
def get_student_course_data_table() -> DataTable:
    """Creates a mail merge data source."""

    data_table = DataTable("StudentCourse")
    data_table.columns.add("CourseName")
    for i in range(10):

        datarow = data_table.new_row()
        data_table.rows.add(datarow)
        datarow[0] = "Course " + i

    return data_table
```

Shows how to insert fields, and move the document builder's cursor to them.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.insert_field(r"MERGEFIELD MyMergeField1 \* MERGEFORMAT")
builder.insert_field(r"MERGEFIELD MyMergeField2 \* MERGEFORMAT")

# Move the cursor to the first MERGEFIELD.
builder.move_to_merge_field("MyMergeField1", True, False)

# Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
self.assertEqual(doc.range.fields[1].start, builder.current_node)
self.assertEqual(doc.range.fields[0].end, builder.current_node.previous_sibling)

# If we wish to edit the field's field code or contents using the builder,
# its cursor would need to be inside a field.
# To place it inside a field, we would need to call the document builder's "move_to" method
# and pass the field's start or separator node as an argument.
builder.write(" Text between our merge fields. ")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.merge_fields.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

