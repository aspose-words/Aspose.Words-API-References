---
title: field_value property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the value of the field from the data source."
type: docs
weight: 50
url: /python-net/aspose.words.mailmerging/fieldmergingargsbase/field_value/
---

## FieldMergingArgsBase.field_value property

Gets or sets the value of the field from the data source.

This property contains a value that has just been selected from your data source
for this field by the mail merge engine. You can also replace the value by setting the property.


### Examples

Shows how to edit values that MERGEFIELDs receive as a mail merge takes place.

```python
def test_field_formats(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Insert some MERGEFIELDs with format switches that will edit the values they will receive during a mail merge.
    builder.insert_field("MERGEFIELD text_Field1 \\* Caps", None)
    builder.write(", ")
    builder.insert_field("MERGEFIELD text_Field2 \\* Upper", None)
    builder.write(", ")
    builder.insert_field("MERGEFIELD numeric_Field1 \\# 0.0", None)

    builder.document.mail_merge.field_merging_callback = ExMailMergeEvent.FieldValueMergingCallback()

    builder.document.mail_merge.execute(
        ["text_Field1", "text_Field2", "numeric_Field1"],
        ["Field 1", "Field 2", 10])

    self.assertEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.get_text().strip())

class FieldValueMergingCallback(aw.mailmerging.IFieldMergingCallback):
    """Edits the values that MERGEFIELDs receive during a mail merge.
    The name of a MERGEFIELD must have a prefix for this callback to take effect on its value."""

    def field_merging(self, args: aw.mailmerging.FieldMergingArgs):
        """Called when a mail merge merges data into a MERGEFIELD."""

        if args.field_name.startswith("text_"):
            args.field_value = f"Merge value for \"{args.field_name}\": {args.field_value}"
        elif args.field_name.startswith("numeric_"):
            args.field_value = int(args.field_value) * 1000

    def image_field_merging(self, args: aw.mailmerging.ImageFieldMergingArgs):

        # Do nothing.
        pass
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [FieldMergingArgsBase](../)

