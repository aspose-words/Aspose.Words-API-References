---
title: OdsoRecipientData Class
linktitle: OdsoRecipientData
articleTitle: OdsoRecipientData
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Settings.OdsoRecipientData class, designed to manage and exclude specific records in mail merges for efficient document processing.
type: docs
weight: 6760
url: /net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Represents information about a single record within an external data source that is to be excluded from the mail merge.

To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) documentation article.

```csharp
public class OdsoRecipientData
```

## Constructors

| Name | Description |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is `true`. |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Specifies the column within the data source that contains unique data for the current record. The default value is 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Represents the hash code for this record. Sometimes Microsoft Word uses [`Hash`](./hash/) of a whole record instead of a [`UniqueTag`](./uniquetag/) value. The default value is 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Specifies the contents of a given record in the column containing unique data. The default value is `null`. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Returns a deep clone of this object. |

## Remarks

If a record shall be merged into a merged document, then no information is needed about that record. However, if a given record shall not be merged into a merged document, then the value of the unique key for that record shall be stored in the [`UniqueTag`](./uniquetag/) property of this object to indicate this exclusion.

## Examples

Shows how to access the collection of data that designates which merge data source records a mail merge will exclude.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.That(dataCollection.Count, Is.EqualTo(70));

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// We can clone the elements in this collection.
Assert.That(dataCollection[0].Clone(), Is.Not.EqualTo(dataCollection[0]));

// We can also remove elements individually, or clear the entire collection at once.
dataCollection.RemoveAt(0);

Assert.That(dataCollection.Count, Is.EqualTo(69));

dataCollection.Clear();

Assert.That(dataCollection.Count, Is.EqualTo(0));
```

### See Also

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
