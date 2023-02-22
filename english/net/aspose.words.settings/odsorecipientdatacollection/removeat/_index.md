---
title: RemoveAt
second_title: Aspose.Words for .NET API Reference
description: OdsoRecipientDataCollection method. Removes the element at the specified index in C#.
type: docs
weight: 70
url: /net/aspose.words.settings/odsorecipientdatacollection/removeat/
---
## OdsoRecipientDataCollection.RemoveAt method

Removes the element at the specified index.

```csharp
public void RemoveAt(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the element. |

## Examples

Shows how to access the collection of data that designates which merge data source records a mail merge will exclude.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

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
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// We can also remove elements individually, or clear the entire collection at once.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### See Also

* class [OdsoRecipientDataCollection](../)
* namespace [Aspose.Words.Settings](../../odsorecipientdatacollection/)
* assembly [Aspose.Words](../../../)
