---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.OdsoFieldMapData für die nahtlose Zuordnung externer Datenspalten zu vordefinierten Dokumentserienfeldern und verbessern Sie so Ihre Dokumentautomatisierung.
type: docs
weight: 6730
url: /de/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Gibt an, wie eine Spalte in der externen Datenquelle den vordefinierten Seriendruckfeldern im Dokument zugeordnet werden soll.

Um mehr zu erfahren, besuchen Sie die[Serienbriefe und Berichte](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

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
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Gibt den nullbasierten Index der Spalte innerhalb einer externen Datenquelle an, die dem lokalen Namen eines bestimmten MERGEFIELD-Felds zugeordnet werden soll. Der Standardwert ist 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Gibt den vordefinierten Seriendruckfeldnamen an, der der Spaltennummer zugeordnet werden soll, die durch den[`Column`](./column/) Eigenschaft innerhalb dieser Feldzuordnung. Der Standardwert ist eine leere Zeichenfolge. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Gibt den Spaltennamen innerhalb einer externen Datenquelle für die Spalte an, deren -Index durch den[`Column`](./column/)property. Der Standardwert ist eine leere Zeichenfolge. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Gibt an, ob ein bestimmtes Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. Der Standardwert istDefault . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Gibt einen tiefen Klon dieses Objekts zurück. |

## Bemerkungen

Microsoft Word bietet einige vordefinierte Seriendruckfeldnamen, die in ein Dokument als MERGEFIELD oder in den Feldern ADDRESSBLOCK oder GREETINGLINE eingefügt werden können. Die in`OdsoFieldMapData` ermöglicht die Zuordnung einer Spalte in der externen Datenquelle zu einem einzelnen vordefinierten Seriendruckfeld.

## Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die Datenquellenspalten Seriendruckfeldern zuordnet.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Diese Sammlung definiert, wie ein Serienbrief Spalten aus einer Datenquelle abbildet
// zu vordefinierten MERGEFIELD-, ADDRESSBLOCK- und GREETINGLINE-Feldern.
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

// Verwenden Sie die Elemente der Methode „RemoveAt“ einzeln nach Index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Verwenden Sie die Methode „Clear“, um die gesamte Sammlung auf einmal zu löschen.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
