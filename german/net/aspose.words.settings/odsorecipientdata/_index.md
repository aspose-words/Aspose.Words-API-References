---
title: Class OdsoRecipientData
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.OdsoRecipientData klas. Stellt Informationen zu einem einzelnen Datensatz innerhalb einer externen Datenquelle dar der vom Seriendruck ausgeschlossen werden soll.
type: docs
weight: 5630
url: /de/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Stellt Informationen zu einem einzelnen Datensatz innerhalb einer externen Datenquelle dar, der vom Seriendruck ausgeschlossen werden soll.

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
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Gibt an, ob der Datensatz aus der Datenquelle beim Seriendruck in ein Dokument importiert werden soll. Der Standardwert ist`Stimmt` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Gibt die Spalte innerhalb der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Repräsentiert den Hash-Code für diesen Datensatz. Manchmal wird Microsoft Word verwendet[`Hash`](./hash/) eines ganzen Datensatzes statt a[`UniqueTag`](./uniquetag/) value. Der Standardwert ist 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. Der Standardwert ist`Null` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Gibt einen tiefen Klon dieses Objekts zurück. |

### Bemerkungen

Wenn ein Datensatz zu einem zusammengeführten Dokument zusammengeführt werden soll, sind keine Informationen zu diesem Datensatz erforderlich. Wenn jedoch ein bestimmter Datensatz nicht in ein zusammengeführtes Dokument zusammengeführt werden soll, dann wird der Wert des eindeutigen Schlüssels für diesen Datensatz in gespeichert[`UniqueTag`](./uniquetag/) Eigenschaft dieses Objekts, um diesen Ausschluss anzugeben.

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


