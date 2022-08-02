---
title: unconditional_merge_fields_and_regions property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition."
type: docs
weight: 140
url: /python-net/aspose.words.mailmerging/mailmerge/unconditional_merge_fields_and_regions/
---

## MailMerge.unconditional_merge_fields_and_regions property

Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.

The default value is **false**.



### Examples

Shows how to merge fields or regions regardless of the parent IF field's condition.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a MERGEFIELD nested inside an IF field.
# Since the IF field statement is False, it will not display the result of the MERGEFIELD.
# The MERGEFIELD will also not receive any data during a mail merge.
field_if = builder.insert_field(" IF 1 = 2 ").as_field_if()
builder.move_to(field_if.separator)
builder.insert_field(" MERGEFIELD  FullName ")

# If we set the "unconditional_merge_fields_and_regions" flag to "True",
# our mail merge will insert data into non-displayed fields such as our MERGEFIELD as well as all others.
# If we set the "unconditional_merge_fields_and_regions" flag to "False",
# our mail merge will not insert data into MERGEFIELDs hidden by IF fields with false statements.
doc.mail_merge.unconditional_merge_fields_and_regions = count_all_merge_fields

data_table = DataTable()
data_table.columns.add("FullName")
data_table.rows.add("James Bond")

doc.mail_merge.execute(data_table)

doc.save(ARTIFACTS_DIR + "MailMerge.unconditional_merge_fields_and_regions.docx")

self.assertEqual(
    "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015" if count_all_merge_fields else "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.get_text().strip())
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

