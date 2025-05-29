---
title: OdsoRecipientDataCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: OdsoRecipientDataCollection'ınızı Item özelliğimizle zahmetsizce yönetin. Sorunsuz veri işleme için öğeleri kolayca alın veya güncelleyin.
type: docs
weight: 30
url: /tr/net/aspose.words.settings/odsorecipientdatacollection/item/
---
## OdsoRecipientDataCollection indexer

Bu koleksiyondaki bir öğeyi alır veya ayarlar.

```csharp
public OdsoRecipientData this[int index] { get; set; }
```

## Örnekler

Bir posta birleştirme işleminin hangi birleştirme veri kaynağı kayıtlarını hariç tutacağını belirten veri koleksiyonuna nasıl erişileceğini gösterir.

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

// Ayrıca öğeleri tek tek kaldırabilir veya tüm koleksiyonu bir kerede temizleyebiliriz.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ayrıca bakınız

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
