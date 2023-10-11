---
title: Class OdsoFieldMapData
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.OdsoFieldMapData klas. Gibt an wie eine Spalte in der externen Datenquelle den vordefinierten Zusammenführungsfeldern im Dokument zugeordnet werden soll.
type: docs
weight: 5900
url: /de/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Gibt an, wie eine Spalte in der externen Datenquelle den vordefinierten Zusammenführungsfeldern im Dokument zugeordnet werden soll.

Um mehr zu erfahren, besuchen Sie die[Serienbrief und Berichterstellung](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class OdsoFieldMapData
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Felds zugeordnet werden soll. Der Standardwert ist 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Gibt den vordefinierten Namen des Zusammenführungsfelds an, der der durch den angegebenen Spaltennummer zugeordnet werden soll[`Column`](./column/) Eigenschaft innerhalb dieser Feldzuordnung. Der Standardwert ist eine leere Zeichenfolge. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Gibt den Spaltennamen innerhalb einer externen Datenquelle für die Spalte an, deren -Index durch angegeben wird[`Column`](./column/)property. Der Standardwert ist eine leere Zeichenfolge. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Gibt an, ob ein bestimmtes Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. Der Standardwert istDefault . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Gibt einen tiefen Klon dieses Objekts zurück. |

### Bemerkungen

Microsoft Word bietet einige vordefinierte Briefvorlagenfeldnamen, die als MERGEFIELD oder in ein Dokument eingefügt werden können und in den Feldern ADDRESSBLOCK oder GREETINGLINE verwendet werden. Die angegebenen Informationen in`OdsoFieldMapData` ermöglicht die Zuordnung einer Spalte in der externen Datenquelle zu einem einzelnen vordefinierten Zusammenführungsfeld.

### Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die Datenquellenspalten Briefvorlagenfeldern zuordnet.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Diese Sammlung definiert, wie ein Serienbrief Spalten aus einer Datenquelle zuordnet
// zu den vordefinierten Feldern MERGEFIELD, ADDRESSBLOCK und GREETINGLINE.
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

// Klonen Sie die Elemente in dieser Sammlung.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Die Elemente der Methode „RemoveAt“ einzeln nach Index verwenden.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Verwenden Sie die Methode „Clear“, um die gesamte Sammlung auf einmal zu löschen.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


