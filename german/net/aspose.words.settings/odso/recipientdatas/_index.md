---
title: Odso.RecipientDatas
second_title: Aspose.Words für .NET-API-Referenz
description: Odso eigendom. Ruft eine Sammlung von Objekten ab oder legt diese fest die den Einschluss/Ausschluss einzelner Datensätze in den Seriendruck festlegen. Dieses Objekt ist niemals null.
type: docs
weight: 70
url: /de/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Ruft eine Sammlung von Objekten ab oder legt diese fest, die den Einschluss/Ausschluss einzelner Datensätze in den Seriendruck festlegen. Dieses Objekt ist niemals null.

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
```

### Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die angibt, welche Zusammenführungsdatenquellen-Datensätze bei einem Seriendruck ausgeschlossen werden.

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

// Wir können auch einzelne Elemente entfernen oder die gesamte Sammlung auf einmal löschen.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* namensraum [Aspose.Words.Settings](../../odso/)
* Montage [Aspose.Words](../../../)


