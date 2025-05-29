---
title: OdsoFieldMapData.Column
linktitle: Column
articleTitle: Column
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der OdsoFieldMapData-Spalteneigenschaft externe Datenquellen mühelos MERGEFIELD-Feldern zuordnen. Optimieren Sie noch heute Ihre Datenintegration!
type: docs
weight: 20
url: /de/net/aspose.words.settings/odsofieldmapdata/column/
---
## OdsoFieldMapData.Column property

Gibt den nullbasierten Index der Spalte innerhalb einer externen Datenquelle an, die dem lokalen Namen eines bestimmten MERGEFIELD-Felds zugeordnet werden soll. Der Standardwert ist 0.

```csharp
public int Column { get; set; }
```

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

* class [OdsoFieldMapData](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
