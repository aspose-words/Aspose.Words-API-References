---
title: OdsoFieldMapDataCollection Class
linktitle: OdsoFieldMapDataCollection
articleTitle: OdsoFieldMapDataCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words-klassen OdsoFieldMapDataCollection, en kraftfull samling av typfiler för effektiv hantering av OdsoFieldMapData-objekt.
type: docs
weight: 6740
url: /sv/net/aspose.words.settings/odsofieldmapdatacollection/
---
## OdsoFieldMapDataCollection class

En maskinskriven samling av[`OdsoFieldMapData`](../odsofieldmapdata/) objekt.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class OdsoFieldMapDataCollection : IEnumerable<OdsoFieldMapData>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OdsoFieldMapDataCollection](odsofieldmapdatacollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.settings/odsofieldmapdatacollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.settings/odsofieldmapdatacollection/item/) { get; set; } | Hämtar eller ställer in ett objekt i den här samlingen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.settings/odsofieldmapdatacollection/add/)(*[OdsoFieldMapData](../odsofieldmapdata/)*) | Lägger till ett objekt i slutet av den här samlingen. |
| [Clear](../../aspose.words.settings/odsofieldmapdatacollection/clear/)() | Tar bort alla element från den här samlingen. |
| [GetEnumerator](../../aspose.words.settings/odsofieldmapdatacollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [RemoveAt](../../aspose.words.settings/odsofieldmapdatacollection/removeat/)(*int*) | Tar bort elementet vid det angivna indexet. |

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

* class [OdsoFieldMapData](../odsofieldmapdata/)
* property [FieldMapDatas](../odso/fieldmapdatas/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
