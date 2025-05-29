---
title: Odso.FieldMapDatas
linktitle: FieldMapDatas
articleTitle: FieldMapDatas
second_title: Aspose.Words für .NET
description: Entdecken Sie Odso FieldMapDatas, ordnen Sie externe Datenspalten mühelos vordefinierten Seriendruckfeldern zu und sorgen Sie so für eine nahtlose Dokumentintegration und verbesserte Datengenauigkeit.
type: docs
weight: 50
url: /de/net/aspose.words.settings/odso/fieldmapdatas/
---
## Odso.FieldMapDatas property

Ruft eine Sammlung von Objekten ab oder legt diese fest, die angeben, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. Dieses Objekt wird nie`null` .

```csharp
public OdsoFieldMapDataCollection FieldMapDatas { get; set; }
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

* class [OdsoFieldMapDataCollection](../../odsofieldmapdatacollection/)
* class [Odso](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
