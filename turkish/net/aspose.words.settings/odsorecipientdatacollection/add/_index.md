---
title: Add
second_title: Aspose.Words for .NET API Referansı
description: Bu koleksiyonun sonuna bir nesne ekler.
type: docs
weight: 40
url: /tr/net/aspose.words.settings/odsorecipientdatacollection/add/
---
## OdsoRecipientDataCollection.Add method

Bu koleksiyonun sonuna bir nesne ekler.

```csharp
public int Add(OdsoRecipientData value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| value | OdsoRecipientData | Eklenecek nesne. Boş olamaz. |

### Örnekler

Adres mektup birleştirmenin hangi birleştirme veri kaynağı kayıtlarını dışlayacağını belirleyen veri koleksiyonuna nasıl erişileceğini gösterir.

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

// Bu koleksiyondaki elemanları klonlayabiliriz.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Elemanları tek tek kaldırabilir veya tüm koleksiyonu bir kerede temizleyebiliriz.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ayrıca bakınız

* class [OdsoRecipientData](../../odsorecipientdata)
* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection)
* ad alanı [Aspose.Words.Settings](../../odsorecipientdatacollection)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->