﻿---
title: Odso class
linktitle: Odso class
articleTitle: Odso class
second_title: Aspose.Words for Python
description: "aspose.words.settings.Odso class. Specifies the Office Data Source Object (ODSO) settings for a mail merge data source"
type: docs
weight: 120
url: /python-net/aspose.words.settings/odso/
---

## Odso class

Specifies the Office Data Source Object (ODSO) settings for a mail merge data source.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




ODSO seems to be the "new" way the newer Microsoft Word versions prefer to use when specifying certain 
types of data sources for a mail merge document. ODSO probably first appeared in Microsoft Word 2000.

The use of ODSO is poorly documented and the best way to learn how to use the properties of this object 
is to create a document with a desired data source manually in Microsoft Word and then open that document using 
Aspose.Words and examine the properties of the [Document.mail_merge_settings](../../aspose.words/document/mail_merge_settings/) and 
[MailMergeSettings.odso](../mailmergesettings/odso/) objects. This is a good approach to take if you want to learn how to 
programmatically configure a data source, for example.

You do not normally need to create objects of this class directly because ODSO settings
are always available via the [MailMergeSettings.odso](../mailmergesettings/odso/) property.




### Constructors
| Name | Description |
| --- | --- |
| [Odso()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [column_delimiter](./column_delimiter/) | Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. The default value is 0 which means there is no column delimiter defined. |
| [data_source](./data_source/) | Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string. |
| [data_source_type](./data_source_type/) | Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. The default value is [OdsoDataSourceType.DEFAULT](../odsodatasourcetype/#DEFAULT). |
| [field_map_datas](./field_map_datas/) | Gets or sets a collection of objects that specify how columns from the external data source  are mapped to the predefined merge field names in the document. This object is never ``None``. |
| [first_row_contains_column_names](./first_row_contains_column_names/) | Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. The default value is ``False``. |
| [recipient_datas](./recipient_datas/) | Gets or sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never ``None``. |
| [table_name](./table_name/) | Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string. |
| [udl_connect_string](./udl_connect_string/) | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

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

* module [aspose.words.settings](../)
* property [MailMergeSettings.odso](../mailmergesettings/odso/)

