---
title: Odso class
linktitle: Odso class
articleTitle: Odso class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.Odso class. Specifies the Office Data Source Object (ODSO) settings for a mail merge data source"
type: docs
weight: 120
url: /nodejs-net/aspose.words.settings/odso/
---

## Odso class

Specifies the Office Data Source Object (ODSO) settings for a mail merge data source.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/nodejs-net/mail-merge-and-reporting/) documentation article.




### Remarks

ODSO seems to be the "new" way the newer Microsoft Word versions prefer to use when specifying certain 
types of data sources for a mail merge document. ODSO probably first appeared in Microsoft Word 2000.

The use of ODSO is poorly documented and the best way to learn how to use the properties of this object 
is to create a document with a desired data source manually in Microsoft Word and then open that document using 
Aspose.Words and examine the properties of the [Document.mailMergeSettings](../../aspose.words/document/mailMergeSettings/) and 
[MailMergeSettings.odso](../mailmergesettings/odso/) objects. This is a good approach to take if you want to learn how to 
programmatically configure a data source, for example.

You do not normally need to create objects of this class directly because ODSO settings
are always available via the [MailMergeSettings.odso](../mailmergesettings/odso/) property.




### Constructors
| Name | Description |
| --- | --- |
| [Odso()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [columnDelimiter](./columnDelimiter/) | Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. The default value is 0 which means there is no column delimiter defined. |
| [dataSource](./dataSource/) | Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string. |
| [dataSourceType](./dataSourceType/) | Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. The default value is [OdsoDataSourceType.Default](../odsodatasourcetype/#Default). |
| [fieldMapDatas](./fieldMapDatas/) | Gets or sets a collection of objects that specify how columns from the external data source  are mapped to the predefined merge field names in the document. This object is never ``null``. |
| [firstRowContainsColumnNames](./firstRowContainsColumnNames/) | Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. The default value is ``false``. |
| [recipientDatas](./recipientDatas/) | Gets or sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never ``null``. |
| [tableName](./tableName/) | Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string. |
| [udlConnectString](./udlConnectString/) | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

### See Also

* module [Aspose.Words.Settings](../)
* property [MailMergeSettings.odso](../mailmergesettings/odso/)

