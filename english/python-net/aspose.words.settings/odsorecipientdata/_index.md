---
title: OdsoRecipientData class
linktitle: OdsoRecipientData class
articleTitle: OdsoRecipientData class
second_title: Aspose.Words for Python
description: "aspose.words.settings.OdsoRecipientData class. Represents information about a single record within an external data source that is to be excluded from the mail merge"
type: docs
weight: 170
url: /python-net/aspose.words.settings/odsorecipientdata/
---

## OdsoRecipientData class

Represents information about a single record within an external data source that is to be excluded from the mail merge.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




### Remarks

If a record shall be merged into a merged document, then no information is needed about that record. 
However, if a given record shall not be merged into a merged document, then the value of the unique key 
for that record shall be stored in the [OdsoRecipientData.unique_tag](./unique_tag/) property of this object to indicate this exclusion.




### Constructors
| Name | Description |
| --- | --- |
| [OdsoRecipientData()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [active](./active/) | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is ``True``. |
| [column](./column/) | Specifies the column within the data source that contains unique data for the current record. The default value is 0. |
| [hash](./hash/) | Represents the hash code for this record.  Sometimes Microsoft Word uses [OdsoRecipientData.hash](./hash/) of a whole record instead of a [OdsoRecipientData.unique_tag](./unique_tag/) value. The default value is 0. |
| [unique_tag](./unique_tag/) | Specifies the contents of a given record in the column containing unique data. The default value is ``None``. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

### See Also

* module [aspose.words.settings](../)

