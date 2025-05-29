---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.OdsoFieldMappingType-enum för effektiv mappning av fält för dokumentkoppling till externa datakällor. Förbättra din dokumentautomation idag!
type: docs
weight: 6750
url: /sv/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Anger de möjliga typer som används för att indikera om ett givet fält för koppling av dokument har mappats till en kolumn i den givna externa datakällan.

```csharp
public enum OdsoFieldMappingType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Column | `0` | Anger att fältet för dokumentkoppling har mappats till en kolumn i den angivna externa datakällan. |
| Null | `1` | Anger att fältet för dokumentkoppling inte har mappats till en kolumn i den angivna externa datakällan. |
| Default | `1` | är lika medNull . |

## Exempel

Visar hur man kommer åt datasamlingen som mappar datakällkolumner till kopplingsfält.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Denna samling definierar hur en dokumentkoppling mappar kolumner från en datakälla
// till fördefinierade fält MERGEFIELD, ADDRESSBLOCK och GREETEINGLINE.
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

// Klona elementen i den här samlingen.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Använd metodelementen "RemoveAt" individuellt efter index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Använd metoden "Rensa" för att rensa hela samlingen på en gång.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Se även

* property [Type](../odsofieldmapdata/type/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
