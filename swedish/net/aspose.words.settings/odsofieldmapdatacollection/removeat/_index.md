---
title: OdsoFieldMapDataCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words för .NET
description: Använd enkelt RemoveAt-metoden i OdsoFieldMapDataCollection för att ta bort element efter index, vilket effektiviserar dina datahanteringsuppgifter.
type: docs
weight: 70
url: /sv/net/aspose.words.settings/odsofieldmapdatacollection/removeat/
---
## OdsoFieldMapDataCollection.RemoveAt method

Tar bort elementet vid det angivna indexet.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Elementets nollbaserade index. |

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

* class [OdsoFieldMapDataCollection](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
