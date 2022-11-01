---
title: use_non_merge_fields property
second_title: Aspose.Words for Python via .NET API Reference
description: "When ``True``, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into {{fieldName}} tags."
type: docs
weight: 150
url: /python-net/aspose.words.mailmerging/mailmerge/use_non_merge_fields/
---

## MailMerge.use_non_merge_fields property

When ``True``, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and
also into "{{fieldName}}" tags.


Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting
built using other fields and had many documents created this way. To simplify migration (and because this
approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [MailMerge.use_non_merge_fields](./) is set to ``True``, Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Also, when [MailMerge.use_non_merge_fields](./) is set to ``True``, Aspose.Words will perform mail merge into text tags
"{{fieldName}}". These are not fields, but just text tags.




### Examples

Shows how to preserve the appearance of alternative mail merge tags that go unused during a mail merge.

```python
def test_preserve_unused_tags(self):

    for preserve_unused_tags in (False, True):
        with self.subTest(preserve_unused_tags=preserve_unused_tags):
            doc = ExMailMerge.create_source_doc_with_alternative_merge_fields()
            data_table = ExMailMerge.create_source_table_preserve_unused_tags()

            # By default, a mail merge places data from each row of a table into MERGEFIELDs, which name columns in that table.
            # Our document has no such fields, but it does have plaintext tags enclosed by curly braces.
            # If we set the "preserve_unused_tags" flag to "True", we could treat these tags as MERGEFIELDs
            # to allow our mail merge to insert data from the data source at those tags.
            # If we set the "preserve_unused_tags" flag to "False",
            # the mail merge will convert these tags to MERGEFIELDs and leave them unfilled.
            doc.mail_merge.preserve_unused_tags = preserve_unused_tags
            doc.mail_merge.execute(data_table)

            doc.save(ARTIFACTS_DIR + "MailMerge.preserve_unused_tags.docx")

            # Our document has a tag for a column named "Column2", which does not exist in the table.
            # If we set the "preserve_unused_tags" flag to "False", then the mail merge will convert this tag into a MERGEFIELD.
            self.assertEqual(doc.get_text().contains("{{ Column2 }}"), preserve_unused_tags)

            if preserve_unused_tags:
                self.assertEqual(0, len([f for f in doc.range.fields if f.type == aw.fields.field_type.FIELD_MERGE_FIELD]))
            else:
                self.assertEqual(1, len([f for f in doc.range.fields if f.type == aw.fields.field_type.FIELD_MERGE_FIELD]))

@staticmethod
def create_source_doc_with_alternative_merge_fields() -> aw.Document:
    """Create a document and add two plaintext tags that may act as MERGEFIELDs during a mail merge."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.writeln("{{ Column1 }}")
    builder.writeln("{{ Column2 }}")

    # Our tags will register as destinations for mail merge data only if we set this to True.
    doc.mail_merge.use_non_merge_fields = True

    return doc

@staticmethod
def create_source_table_preserve_unused_tags() -> DataTable:
    """Create a simple data table with one column."""

    data_table = DataTable("MyTable")
    data_table.columns.add("Column1")
    data_table.rows.add(["Value1"])

    return data_table
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

