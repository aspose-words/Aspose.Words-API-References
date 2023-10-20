---
title: OdsoFieldMapData.MappedName
linktitle: MappedName
articleTitle: MappedName
second_title: Aspose.Words för .NET
description: OdsoFieldMapData MappedName fast egendom. Anger det fördefinierade sammanslagningsfältets namn som ska mappas till kolumnnumret som anges avColumn egenskap inom denna fältmappning. Standardvärdet är en tom sträng i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.settings/odsofieldmapdata/mappedname/
---
## OdsoFieldMapData.MappedName property

Anger det fördefinierade sammanslagningsfältets namn som ska mappas till kolumnnumret som anges av[`Column`](../column/) egenskap inom denna fältmappning. Standardvärdet är en tom sträng.

```csharp
public string MappedName { get; set; }
```

## Exempel

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

* class [OdsoFieldMapData](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
