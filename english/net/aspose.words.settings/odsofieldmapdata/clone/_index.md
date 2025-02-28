---
title: OdsoFieldMapData.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Effortlessly create a deep clone of your OdsoFieldMapData object with our Clone method. Enhance your data management with precision and ease.
type: docs
weight: 60
url: /net/aspose.words.settings/odsofieldmapdata/clone/
---
## OdsoFieldMapData.Clone method

Returns a deep clone of this object.

```csharp
public OdsoFieldMapData Clone()
```

## Examples

Shows how to access the collection of data that maps data source columns to merge fields.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// This collection defines how a mail merge will map columns from a data source
// to predefined MERGEFIELD, ADDRESSBLOCK and GREETINGLINE fields.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// Clone the elements in this collection.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Use the "RemoveAt" method elements individually by index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Use the "Clear" method to clear the entire collection at once.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### See Also

* class [OdsoFieldMapData](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
