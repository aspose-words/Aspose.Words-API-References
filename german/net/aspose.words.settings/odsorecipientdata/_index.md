---
title: Class OdsoRecipientData
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.OdsoRecipientData klas. Stellt Informationen zu einem einzelnen Datensatz in einer externen Datenquelle dar der vom Serienbrief ausgeschlossen werden soll.
type: docs
weight: 5930
url: /de/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Stellt Informationen zu einem einzelnen Datensatz in einer externen Datenquelle dar, der vom Serienbrief ausgeschlossen werden soll.

Um mehr zu erfahren, besuchen Sie die[Serienbrief und Berichterstellung](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class OdsoRecipientData
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Gibt an, ob der Datensatz aus der Datenquelle in ein Dokument importiert werden soll, wenn der Seriendruck durchgeführt wird. Der Standardwert ist`WAHR` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Gibt die Spalte innerhalb der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Stellt den Hashcode für diesen Datensatz dar. Manchmal verwendet Microsoft Word[`Hash`](./hash/) eines ganzen Datensatzes statt eines[`UniqueTag`](./uniquetag/) value. Der Standardwert ist 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Gibt den Inhalt eines bestimmten Datensatzes in der Spalte an, die eindeutige Daten enthält. Der Standardwert ist`Null` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Gibt einen tiefen Klon dieses Objekts zurück. |

### Bemerkungen

Wenn ein Datensatz in einem zusammengeführten Dokument zusammengeführt werden soll, sind keine Informationen zu diesem Datensatz erforderlich. Wenn ein bestimmter Datensatz jedoch nicht in einem zusammengeführten Dokument zusammengeführt werden soll, muss der Wert des eindeutigen Schlüssels für diesen Datensatz im gespeichert werden[`UniqueTag`](./uniquetag/)Eigenschaft dieses Objekts, um diesen Ausschluss anzuzeigen.

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


