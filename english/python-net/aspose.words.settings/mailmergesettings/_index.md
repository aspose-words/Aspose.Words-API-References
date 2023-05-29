﻿---
title: MailMergeSettings class
linktitle: MailMergeSettings class
articleTitle: MailMergeSettings class
second_title: Aspose.Words for Python
description: "aspose.words.settings.MailMergeSettings class. Specifies all of the mail merge information for a document"
type: docs
weight: 90
url: /python-net/aspose.words.settings/mailmergesettings/
---

## MailMergeSettings class

Specifies all of the mail merge information for a document.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




You can use this object to specify a mail merge data source for a document and this information
(along with the available data fields) will appear in Microsoft Word when the user opens this document.
Or you can use this object to query mail merge settings that the user has specified in Microsoft Word 
for this document.

You do not normally need to create objects of this class directly because Mail merge settings 
of a document are always available via the [Document.mail_merge_settings](../../aspose.words/document/mail_merge_settings/) property.

To detect whether this document is a mail merge main document, check the value of the 
[MailMergeSettings.main_document_type](./main_document_type/) property.

To remove mail merge settings and data source information from a document you can use the 
[MailMergeSettings.clear()](./clear/#default) method. Aspose.Words will not write mail merge settings to a document if 
the [MailMergeSettings.main_document_type](./main_document_type/) property is set to [MailMergeMainDocumentType.NOT_A_MERGE_DOCUMENT](../mailmergemaindocumenttype/#NOT_A_MERGE_DOCUMENT)
or the [MailMergeSettings.data_type](./data_type/) property is set to [MailMergeDataType.NONE](../mailmergedatatype/#NONE).

The best way to learn how to use the properties of this object is to create a document with a desired 
data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties 
of the [Document.mail_merge_settings](../../aspose.words/document/mail_merge_settings/) and [MailMergeSettings.odso](./odso/) objects. This is 
a good approach to take if you want to learn how to programmatically configure a data source, for example.

Aspose.Words preserves mail merge information when loading, saving and converting documents
between different formats, but does not use this information when performing its own mail merge 
using the [MailMerge](../../aspose.words.mailmerging/mailmerge/) object.




### Constructors
| Name | Description |
| --- | --- |
| [MailMergeSettings()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [active_record](./active_record/) | Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1. |
| [address_field_name](./address_field_name/) | Specifies the column within the data source that contains e-mail addresses. The default value is an empty string. |
| [check_errors](./check_errors/) | Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge.  The default value is [MailMergeCheckErrors.DEFAULT](../mailmergecheckerrors/#DEFAULT). |
| [connect_string](./connect_string/) | Specifies the connection string used to connect to an external data source. The default value is an empty string. |
| [data_source](./data_source/) | Specifies the path to the mail-merge data source. The default value is an empty string. |
| [data_type](./data_type/) | Specifies the type of the mail-merge data source and the method of data access. The default value is [MailMergeDataType.DEFAULT](../mailmergedatatype/#DEFAULT). |
| [destination](./destination/) | Specifies how Microsoft Word will output the results of a mail merge. The default value is [MailMergeDestination.DEFAULT](../mailmergedestination/#DEFAULT). |
| [do_not_supress_blank_lines](./do_not_supress_blank_lines/) | Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. The default value is ``False``. |
| [header_source](./header_source/) | Specifies the path to the mail-merge header source. The default value is an empty string. |
| [link_to_query](./link_to_query/) | Not sure about this one. The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document  is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference to an external query file which contains the actual query. The default value is ``False``. |
| [mail_as_attachment](./mail_as_attachment/) | Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather  than the body of the actual e-mail. The default value is ``False``. |
| [mail_subject](./mail_subject/) | Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. The default value is an empty string. |
| [main_document_type](./main_document_type/) | Specifies the mail-merge main document type.  The default value is [MailMergeMainDocumentType.DEFAULT](../mailmergemaindocumenttype/#DEFAULT). |
| [odso](./odso/) | Gets or sets the object that specifies the Office Data Source Object (ODSO) settings. |
| [query](./query/) | Contains the Structured Query Language string that shall be run against the specified external data source to  return the set of records which shall be imported into the document when the mail merge operation is performed. The default value is an empty string. |
| [view_merged_data](./view_merged_data/) | Specifies that Microsoft Word shall display the data from the specified external data source where merge fields  have been inserted (e.g. preview merged data). The default value is ``False``. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Clears the mail merge settings in such a way that when the document is saved,  no mail merge settings will be saved and it will become a normal document. |
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
* property [Document.mail_merge_settings](../../aspose.words/document/mail_merge_settings/)

