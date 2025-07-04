---
title: Odso.RecipientDatas
linktitle: RecipientDatas
articleTitle: RecipientDatas
second_title: Aspose.Words for .NET
description: Manage your mail merge effortlessly with Odso RecipientDatas. Control inclusion/exclusion of records with a reliable, always-available collection.
type: docs
weight: 70
url: /net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Gets or sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never `null`.

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
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

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
