---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.OdsoFieldMapData för sömlös mappning av externa datakolumner till fördefinierade dokumentkopplingsfält, vilket förbättrar din dokumentautomation.
type: docs
weight: 6730
url: /sv/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Anger hur en kolumn i den externa datakällan ska mappas till de fördefinierade kopplingsfälten i dokumentet.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class OdsoFieldMapData
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Anger det nollbaserade indexet för kolumnen inom en extern datakälla som ska mappas till det lokala namnet på ett specifikt MERGEFIELD-fält. Standardvärdet är 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Anger det fördefinierade kopplingsfältnamnet som ska mappas till kolumnnumret som anges av[`Column`](./column/) egenskap inom denna fältmappning. Standardvärdet är en tom sträng. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Anger kolumnnamnet i en extern datakälla för den kolumn vars -index anges av[`Column`](./column/)property. Standardvärdet är en tom sträng. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Anger om ett givet fält för koppling av dokument har mappats till en kolumn i den angivna externa datakällan eller inte. Standardvärdet ärDefault . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Returnerar en djup klon av detta objekt. |

## Anmärkningar

Microsoft Word tillhandahåller några fördefinierade namn på kopplingsfält som det gör att man kan infoga i ett dokument som MERGEFIELD eller i fälten ADRESSBLOCK eller HÄLSNINGSLINJE. Informationen som anges i`OdsoFieldMapData` gör det möjligt att mappa en kolumn i den externa datakällan till ett enda fördefinierat kopplingsfält.

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

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
