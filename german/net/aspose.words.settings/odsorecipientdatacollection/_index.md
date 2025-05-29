---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Settings.OdsoRecipientDataCollection, eine leistungsstarke typisierte Sammlung zur effizienten Verwaltung von OdsoRecipientData in Ihren Anwendungen.
type: docs
weight: 6770
url: /de/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

Eine typisierte Sammlung von[`OdsoRecipientData`](../odsorecipientdata/)

Um mehr zu erfahren, besuchen Sie die[Serienbriefe und Berichte](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Ruft ein Element in dieser Sammlung ab oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | Fügt am Ende dieser Sammlung ein Objekt hinzu. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Entfernt alle Elemente aus dieser Sammlung. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | Entfernt das Element am angegebenen Index. |

## Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die angibt, welche Datensätze aus Seriendruckdatenquellen bei einem Seriendruck ausgeschlossen werden.

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

// Wir können Elemente auch einzeln entfernen oder die gesamte Sammlung auf einmal löschen.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* class [OdsoRecipientData](../odsorecipientdata/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
