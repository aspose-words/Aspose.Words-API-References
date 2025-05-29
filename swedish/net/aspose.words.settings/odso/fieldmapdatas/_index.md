---
title: Odso.FieldMapDatas
linktitle: FieldMapDatas
articleTitle: FieldMapDatas
second_title: Aspose.Words för .NET
description: Upptäck Odso FieldMapDatas, mappa enkelt externa datakolumner till fördefinierade kopplingsfält, vilket säkerställer sömlös dokumentintegration och förbättrad datanoggrannhet.
type: docs
weight: 50
url: /sv/net/aspose.words.settings/odso/fieldmapdatas/
---
## Odso.FieldMapDatas property

Hämtar eller anger en samling objekt som anger hur kolumner från den externa datakällan mappas till de fördefinierade kopplingsfältnamnen i dokumentet. Detta objekt mappas aldrig`null` .

```csharp
public OdsoFieldMapDataCollection FieldMapDatas { get; set; }
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

* class [OdsoFieldMapDataCollection](../../odsofieldmapdatacollection/)
* class [Odso](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
