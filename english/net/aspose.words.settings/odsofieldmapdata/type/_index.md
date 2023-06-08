---
title: OdsoFieldMapData.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: OdsoFieldMapData Type property. Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is Default in C#.
type: docs
weight: 50
url: /net/aspose.words.settings/odsofieldmapdata/type/
---
## OdsoFieldMapData.Type property

Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is Default.

```csharp
public OdsoFieldMappingType Type { get; set; }
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

* enum [OdsoFieldMappingType](../../odsofieldmappingtype/)
* class [OdsoFieldMapData](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
