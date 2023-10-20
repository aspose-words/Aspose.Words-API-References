---
title: OdsoFieldMapData.MappedName
linktitle: MappedName
articleTitle: MappedName
second_title: Aspose.Words für .NET
description: OdsoFieldMapData MappedName eigendom. Gibt den vordefinierten Namen des Zusammenführungsfelds an der der durch den angegebenen Spaltennummer zugeordnet werden sollColumn Eigenschaft innerhalb dieser Feldzuordnung. Der Standardwert ist eine leere Zeichenfolge in C#.
type: docs
weight: 30
url: /de/net/aspose.words.settings/odsofieldmapdata/mappedname/
---
## OdsoFieldMapData.MappedName property

Gibt den vordefinierten Namen des Zusammenführungsfelds an, der der durch den angegebenen Spaltennummer zugeordnet werden soll[`Column`](../column/) Eigenschaft innerhalb dieser Feldzuordnung. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string MappedName { get; set; }
```

## Beispiele

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

* class [OdsoFieldMapData](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
