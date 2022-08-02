---
title: link_to_query property
second_title: Aspose.Words for Python via .NET API Reference
description: "Not sure about this one"
type: docs
weight: 110
url: /python-net/aspose.words.settings/mailmergesettings/link_to_query/
---

## MailMergeSettings.link_to_query property

Not sure about this one.
The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document 
is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference
to an external query file which contains the actual query.
The default value is ``false``.



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

