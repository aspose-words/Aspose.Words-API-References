---
title: FieldMergingArgsBase.record_index property
linktitle: record_index property
articleTitle: record_index property
second_title: Aspose.Words for Python
description: "FieldMergingArgsBase.record_index property. Gets the zero based index of the record that is being merged."
type: docs
weight: 60
url: /python-net/aspose.words.mailmerging/fieldmergingargsbase/record_index/
---

## FieldMergingArgsBase.record_index property

Gets the zero based index of the record that is being merged.


### Examples

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

### See Also

* module [aspose.words.mailmerging](../../)
* class [FieldMergingArgsBase](../)

