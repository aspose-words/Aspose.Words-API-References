---
title: MailMergeSettings.view_merged_data property
linktitle: view_merged_data property
articleTitle: view_merged_data property
second_title: Aspose.Words for Python
description: "MailMergeSettings.view_merged_data property. Specifies that Microsoft Word shall display the data from the specified external data source where merge fields  have been inserted (e.g"
type: docs
weight: 170
url: /python-net/aspose.words.settings/mailmergesettings/view_merged_data/
---

## MailMergeSettings.view_merged_data property

Specifies that Microsoft Word shall display the data from the specified external data source where merge fields 
have been inserted (e.g. preview merged data). The default value is ``False``.



### Examples

Shows how to execute a mail merge with data from an Office Data Source Object.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Dear ")
builder.insert_field("MERGEFIELD FirstName", "<FirstName>")
builder.write(" ")
builder.insert_field("MERGEFIELD LastName", "<LastName>")
builder.writeln(": ")
builder.insert_field("MERGEFIELD Message", "<Message>")

# Create a data source in the form of an ASCII file, with the "|" character
# acting as the delimiter that separates columns. The first line contains the three columns' names,
# and each subsequent line is a row with their respective values.
lines = [
    "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge."
    ]
data_src_filename = ARTIFACTS_DIR + "MailMerge.mail_merge_settings.data_source.txt"

with open(data_src_filename, "wt") as file:
    file.writelines(lines)

settings = doc.mail_merge_settings
settings.main_document_type = aw.settings.MailMergeMainDocumentType.MAILING_LABELS
settings.check_errors = aw.settings.MailMergeCheckErrors.SIMULATE
settings.data_type = aw.settings.MailMergeDataType.NATIVE
settings.data_source = data_src_filename
settings.query = "SELECT * FROM " + doc.mail_merge_settings.data_source
settings.link_to_query = True
settings.view_merged_data = True

self.assertEqual(aw.settings.MailMergeDestination.DEFAULT, settings.destination)
self.assertFalse(settings.do_not_supress_blank_lines)

odso = settings.odso
odso.data_source = data_src_filename
odso.data_source_type = aw.settings.OdsoDataSourceType.TEXT
odso.column_delimiter = '|'
odso.first_row_contains_column_names = True

#Assert.are_not_same(odso, odso.clone())
#Assert.are_not_same(settings, settings.clone())

# Opening this document in Microsoft Word will execute the mail merge before displaying the contents.
doc.save(ARTIFACTS_DIR + "MailMerge.mail_merge_settings.docx")
```

### See Also

* module [aspose.words.settings](../../)
* class [MailMergeSettings](../)

