---
title: OdsoFieldMapData.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: Discover the OdsoFieldMapData Name property, easily link external data columns with customizable indexing. Simplify data management effortlessly!
type: docs
weight: 40
url: /net/aspose.words.settings/odsofieldmapdata/name/
---
## OdsoFieldMapData.Name property

Specifies the column name within an external data source for the column whose index is specified by the [`Column`](../column/) property. The default value is an empty string.

```csharp
public string Name { get; set; }
```

## Examples

Shows how to access the collection of data that maps data source columns to merge fields.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// This collection defines how a mail merge will map columns from a data source
// to predefined MERGEFIELD, ADDRESSBLOCK and GREETINGLINE fields.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.That(dataCollection.Count, Is.EqualTo(30));

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
Assert.That(dataCollection[0].Clone(), Is.Not.EqualTo(dataCollection[0]));

// Use the "RemoveAt" method elements individually by index.
dataCollection.RemoveAt(0);

Assert.That(dataCollection.Count, Is.EqualTo(29));

// Use the "Clear" method to clear the entire collection at once.
dataCollection.Clear();

Assert.That(dataCollection.Count, Is.EqualTo(0));
```

### See Also

* class [OdsoFieldMapData](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
