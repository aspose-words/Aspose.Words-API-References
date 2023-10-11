---
title: Enum OdsoFieldMappingType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.OdsoFieldMappingType opsomming. Gibt die möglichen Typen an die verwendet werden um anzuzeigen ob ein bestimmtes Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde.
type: docs
weight: 5920
url: /de/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Gibt die möglichen Typen an, die verwendet werden, um anzuzeigen, ob ein bestimmtes Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde.

```csharp
public enum OdsoFieldMappingType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Column | `0` | Gibt an, dass das Serienbrieffeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde. |
| Null | `1` | Gibt an, dass das Serienbrieffeld keiner Spalte in der angegebenen externen Datenquelle zugeordnet wurde. |
| Default | `1` | EntsprichtNull . |

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

* property [Type](../odsofieldmapdata/type/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


