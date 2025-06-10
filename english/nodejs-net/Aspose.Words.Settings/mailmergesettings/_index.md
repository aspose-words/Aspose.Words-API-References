---
title: MailMergeSettings class
linktitle: MailMergeSettings class
articleTitle: MailMergeSettings class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.MailMergeSettings class. Specifies all of the mail merge information for a document"
type: docs
weight: 90
url: /nodejs-net/aspose.words.settings/mailmergesettings/
---

## MailMergeSettings class

Specifies all of the mail merge information for a document.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/nodejs-net/mail-merge-and-reporting/) documentation article.




### Remarks

You can use this object to specify a mail merge data source for a document and this information
(along with the available data fields) will appear in Microsoft Word when the user opens this document.
Or you can use this object to query mail merge settings that the user has specified in Microsoft Word 
for this document.

You do not normally need to create objects of this class directly because Mail merge settings 
of a document are always available via the [Document.mailMergeSettings](../../aspose.words/document/mailMergeSettings/) property.

To detect whether this document is a mail merge main document, check the value of the 
[MailMergeSettings.mainDocumentType](./mainDocumentType/) property.

To remove mail merge settings and data source information from a document you can use the 
[MailMergeSettings.clear()](./clear/#default) method. Aspose.Words will not write mail merge settings to a document if 
the [MailMergeSettings.mainDocumentType](./mainDocumentType/) property is set to [MailMergeMainDocumentType.NotAMergeDocument](../mailmergemaindocumenttype/#NotAMergeDocument)
or the [MailMergeSettings.dataType](./dataType/) property is set to [MailMergeDataType.None](../mailmergedatatype/#None).

The best way to learn how to use the properties of this object is to create a document with a desired 
data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties 
of the [Document.mailMergeSettings](../../aspose.words/document/mailMergeSettings/) and [MailMergeSettings.odso](./odso/) objects. This is 
a good approach to take if you want to learn how to programmatically configure a data source, for example.

Aspose.Words preserves mail merge information when loading, saving and converting documents
between different formats, but does not use this information when performing its own mail merge 
using the Aspose.Words.MailMerging.MailMerge object.




### Constructors
| Name | Description |
| --- | --- |
| [MailMergeSettings()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [activeRecord](./activeRecord/) | Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1. |
| [addressFieldName](./addressFieldName/) | Specifies the column within the data source that contains e-mail addresses. The default value is an empty string. |
| [checkErrors](./checkErrors/) | Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge.  The default value is [MailMergeCheckErrors.Default](../mailmergecheckerrors/#Default). |
| [connectString](./connectString/) | Specifies the connection string used to connect to an external data source. The default value is an empty string. |
| [dataSource](./dataSource/) | Specifies the path to the mail-merge data source. The default value is an empty string. |
| [dataType](./dataType/) | Specifies the type of the mail-merge data source and the method of data access. The default value is [MailMergeDataType.Default](../mailmergedatatype/#Default). |
| [destination](./destination/) | Specifies how Microsoft Word will output the results of a mail merge. The default value is [MailMergeDestination.Default](../mailmergedestination/#Default). |
| [doNotSupressBlankLines](./doNotSupressBlankLines/) | Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. The default value is ``false``. |
| [headerSource](./headerSource/) | Specifies the path to the mail-merge header source. The default value is an empty string. |
| [linkToQuery](./linkToQuery/) | Not sure about this one. The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document  is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference to an external query file which contains the actual query. The default value is ``false``. |
| [mailAsAttachment](./mailAsAttachment/) | Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather  than the body of the actual e-mail. The default value is ``false``. |
| [mailSubject](./mailSubject/) | Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. The default value is an empty string. |
| [mainDocumentType](./mainDocumentType/) | Specifies the mail-merge main document type.  The default value is [MailMergeMainDocumentType.Default](../mailmergemaindocumenttype/#Default). |
| [odso](./odso/) | Gets or sets the object that specifies the Office Data Source Object (ODSO) settings. |
| [query](./query/) | Contains the Structured Query Language string that shall be run against the specified external data source to  return the set of records which shall be imported into the document when the mail merge operation is performed. The default value is an empty string. |
| [viewMergedData](./viewMergedData/) | Specifies that Microsoft Word shall display the data from the specified external data source where merge fields  have been inserted (e.g. preview merged data). The default value is ``false``. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Clears the mail merge settings in such a way that when the document is saved,  no mail merge settings will be saved and it will become a normal document. |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

### See Also

* module [Aspose.Words.Settings](../)
* property [Document.mailMergeSettings](../../aspose.words/document/mailMergeSettings/)

