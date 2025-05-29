---
title: OdsoFieldMapDataCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „OdsoFieldMapDataCollection Count“, um die Gesamtzahl der Elemente in Ihrer Sammlung effizient abzurufen. Optimieren Sie Ihr Datenmanagement noch heute!
type: docs
weight: 20
url: /de/net/aspose.words.settings/odsofieldmapdatacollection/count/
---
## OdsoFieldMapDataCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.

```csharp
public int Count { get; }
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

* class [OdsoFieldMapDataCollection](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
