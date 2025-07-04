---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.OdsoFieldMappingType enum for efficient mail merge field mapping to external data sources. Enhance your document automation today!
type: docs
weight: 6750
url: /net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Specifies the possible types used to indicate if a given mail merge field has been mapped to a column in the given external data source.

```csharp
public enum OdsoFieldMappingType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Column | `0` | Specifies that the mail merge field has been mapped to a column in the given external data source. |
| Null | `1` | Specifies that the mail merge field has not been mapped to a column in the given external data source. |
| Default | `1` | Equals to Null. |

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

* property [Type](../odsofieldmapdata/type/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
