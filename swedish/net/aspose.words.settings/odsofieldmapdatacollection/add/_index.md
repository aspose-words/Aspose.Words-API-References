---
title: OdsoFieldMapDataCollection.Add
second_title: Aspose.Words för .NET API Referens
description: OdsoFieldMapDataCollection metod. Lägger till ett objekt i slutet av den här samlingen.
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
| value | OdsoFieldMapData | Objektet att lägga till. Kan inte vara null. |

### Exempel

Visar hur du får åtkomst till insamlingen av data som mappar datakällans kolumner för att slå samman fält.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Den här samlingen definierar hur en sammanslagning kommer att mappa kolumner från en datakälla
// till fördefinierade fält MERGEFIELD, ADDRESSBLOCK och GREETINGLINE.
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

// Använd "RemoveAt"-metodens element individuellt efter index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Använd "Rensa"-metoden för att rensa hela samlingen på en gång.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Se även

* class [OdsoFieldMapData](../../odsofieldmapdata/)
* class [OdsoFieldMapDataCollection](../)
* namnutrymme [Aspose.Words.Settings](../../odsofieldmapdatacollection/)
* hopsättning [Aspose.Words](../../../)


