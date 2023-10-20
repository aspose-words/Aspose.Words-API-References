---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: Aspose.Words for .NET
description: OdsoRecipientData Hash mülk. Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word kullanırHash bir kayıt yerine tüm bir kaydınUniqueTag değer. Varsayılan değer 0. dir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word kullanır`Hash` bir kayıt yerine tüm bir kaydın[`UniqueTag`](../uniquetag/) değer. Varsayılan değer 0. 'dir

```csharp
public int Hash { get; set; }
```

## Örnekler

Adres-mektup birleştirmenin hangi birleştirme veri kaynağı kayıtlarını hariç tutacağını belirleyen veri koleksiyonuna nasıl erişileceğini gösterir.

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

// Ayrıca öğeleri tek tek kaldırabiliriz veya koleksiyonun tamamını bir kerede temizleyebiliriz.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ayrıca bakınız

* class [OdsoRecipientData](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
