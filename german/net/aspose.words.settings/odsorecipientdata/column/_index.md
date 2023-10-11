---
title: OdsoRecipientData.Column
second_title: Aspose.Words für .NET-API-Referenz
description: OdsoRecipientData eigendom. Gibt die Spalte innerhalb der Datenquelle an die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0.
type: docs
weight: 30
url: /de/net/aspose.words.settings/odsorecipientdata/column/
---
## OdsoRecipientData.Column property

Gibt die Spalte innerhalb der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0.

```csharp
public int Column { get; set; }
```

### Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die angibt, welche Zusammenführungsdatenquellendatensätze von einem Serienbrief ausgeschlossen werden.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Wir können die Elemente in dieser Sammlung klonen.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Wir können auch Elemente einzeln entfernen oder die gesamte Sammlung auf einmal löschen.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* class [OdsoRecipientData](../)
* namensraum [Aspose.Words.Settings](../../odsorecipientdata/)
* Montage [Aspose.Words](../../../)


