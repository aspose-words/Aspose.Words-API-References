---
title: OdsoRecipientDataCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: OdsoRecipientDataCollection Add yöntemi ile veri yönetiminizi zahmetsizce geliştirin; toplama sürecinizi kolaylaştırmak için nesneleri hızla ekleyin.
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
| value | OdsoRecipientData | Eklenecek nesne. Olamaz`hükümsüz`. |

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
