---
title: OdsoFieldMapDataCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Förbättra enkelt din datahantering med OdsoFieldMapDataCollection Add-metoden, utformad för att sömlöst lägga till objekt i din samling.
type: docs
weight: 40
url: /sv/net/aspose.words.settings/odsofieldmapdatacollection/add/
---
## OdsoFieldMapDataCollection.Add method

Lägger till ett objekt i slutet av den här samlingen.

```csharp
public int Add(OdsoFieldMapData value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| value | OdsoFieldMapData | Objektet som ska läggas till. Kan inte vara`null`. |

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

* class [OdsoFieldMapData](../../odsofieldmapdata/)
* class [OdsoFieldMapDataCollection](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
