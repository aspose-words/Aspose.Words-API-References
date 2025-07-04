---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: Aspose.Words for .NET
description: Discover the OdsoRecipientData Hash property, which provides a unique hash code for records, enhancing data integrity in Microsoft Word. Default value, 0.
type: docs
weight: 40
url: /net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

Represents the hash code for this record. Sometimes Microsoft Word uses `Hash` of a whole record instead of a [`UniqueTag`](../uniquetag/) value. The default value is 0.

```csharp
public int Hash { get; set; }
```

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

* class [OdsoRecipientData](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
