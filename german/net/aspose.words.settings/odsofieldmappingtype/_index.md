---
title: Enum OdsoFieldMappingType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.OdsoFieldMappingType opsomming. Gibt die möglichen Typen an die verwendet werden um anzugeben ob ein bestimmtes Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde.
type: docs
weight: 5620
url: /de/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Gibt die möglichen Typen an, die verwendet werden, um anzugeben, ob ein bestimmtes Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde.

```csharp
public enum OdsoFieldMappingType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Column | `0` | Gibt an, dass das Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde. |
| Null | `1` | Gibt an, dass das Seriendruckfeld keiner Spalte in der angegebenen externen Datenquelle zugeordnet wurde. |
| Default | `1` | EntsprichtNull . |

### Beispiele

Zeigt, wie auf die Sammlung von Daten zugegriffen wird, die Datenquellenspalten Briefvorlagenfeldern zuordnet.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Diese Sammlung definiert, wie ein Seriendruck Spalten aus einer Datenquelle zuordnet
// zu vordefinierten MERGEFIELD-, ADRESSBLOCK- und GREETINGLINE-Feldern.
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

// Die Elemente in dieser Sammlung klonen.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Verwenden Sie die "RemoveAt"-Methodenelemente einzeln nach Index.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Verwenden Sie die "Clear"-Methode, um die gesamte Sammlung auf einmal zu löschen.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* property [Type](../odsofieldmapdata/type/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


