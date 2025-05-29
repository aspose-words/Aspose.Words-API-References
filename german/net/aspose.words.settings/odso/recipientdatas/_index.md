---
title: Odso.RecipientDatas
linktitle: RecipientDatas
articleTitle: RecipientDatas
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihren Serienbrief mühelos mit Odso RecipientDatas. Kontrollieren Sie die Einbeziehung/den Ausschluss von Datensätzen mit einer zuverlässigen, stets verfügbaren Sammlung.
type: docs
weight: 70
url: /de/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Ruft eine Sammlung von Objekten ab oder legt sie fest, die die Einbeziehung/den Ausschluss einzelner Datensätze in den Serienbrief festlegen. Dieses Objekt ist nie`null` .

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
```

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

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
