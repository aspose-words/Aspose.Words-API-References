﻿---
title: aspose.words.mailmerging module
linktitle: aspose.words.mailmerging module
articleTitle: aspose.words.mailmerging module
second_title: Aspose.Words for Python
description: "The aspose.words.mailmerging module contains classes of the original mail merge reporting engine."
type: docs
weight: 150
url: /python-net/aspose.words.mailmerging/
---

The **aspose.words.mailmerging** module contains classes of the
"original" mail merge reporting engine.


This reporting engine requires the document to be marked up with Microsoft Word
mail merge fields, but supports more functionality than Microsoft Word's mail merge.

The engine allows to quickly and easily populate a report template with data from various
sources such as **DataTable**, **DataSet**, **DataView**, **IDataReader** or an array of values.


The [MailMerge](./mailmerge/) object which provides access to the reporting functionality
is available via the [Document.mail_merge](../aspose.words/document/mail_merge/) property.


For the newer and more advanced reporting engine based on the LINQ method syntax see
[aspose.words.reporting](../aspose.words.reporting/).





## Classes

| Class | Description |
| --- | --- |
| [FieldMergingArgs](./fieldmergingargs/) | Provides data for the **MergeField** event. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article. |
| [FieldMergingArgsBase](./fieldmergingargsbase/) | Base class for [FieldMergingArgs](./fieldmergingargs/) and [ImageFieldMergingArgs](./imagefieldmergingargs/). To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article. |
| [IFieldMergingCallback](./ifieldmergingcallback/) | Implement this interface if you want to control how data is inserted into merge fields during a mail merge operation. |
| [IMailMergeCallback](./imailmergecallback/) | Implement this interface if you want to receive notifications while mail merge is performed. |
| [IMailMergeDataSource](./imailmergedatasource/) | Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported. |
| [IMailMergeDataSourceRoot](./imailmergedatasourceroot/) | Implement this interface to allow mail merge from a custom data source with master-detail data. |
| [ImageFieldMergingArgs](./imagefieldmergingargs/) | Provides data for the [IFieldMergingCallback.image_field_merging()](./ifieldmergingcallback/image_field_merging/#imagefieldmergingargs) event. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article. |
| [MailMerge](./mailmerge/) | Represents the mail merge functionality. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article. |
| [MailMergeRegionInfo](./mailmergeregioninfo/) | Contains information about a mail merge region. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article. |
| [MappedDataFieldCollection](./mappeddatafieldcollection/) | Allows to automatically map between names of fields in your data source and names of mail merge fields in the document. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article. |
| [MustacheTag](./mustachetag/) | Represents "mustache" tag. |

## Enumerations

| Enumeration | Description |
| --- | --- |
| [MailMergeCleanupOptions](./mailmergecleanupoptions/) | Specifies options that determine what items are removed during mail merge. |

