---
title: OdsoFieldMapData.MappedName
linktitle: MappedName
articleTitle: MappedName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OdsoFieldMapData MappedName, som länkar namn på kopplingsfält till angivna kolumner, vilket förbättrar effektiviteten och noggrannheten i datamappningen.
type: docs
weight: 30
url: /sv/net/aspose.words.settings/odsofieldmapdata/mappedname/
---
## OdsoFieldMapData.MappedName property

Anger det fördefinierade kopplingsfältnamnet som ska mappas till kolumnnumret som anges av[`Column`](../column/) egenskap inom denna fältmappning. Standardvärdet är en tom sträng.

```csharp
public string MappedName { get; set; }
```

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

* class [OdsoFieldMapData](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
