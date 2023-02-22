---
title: OdsoRecipientData.Active
second_title: Aspose.Words for .NET API Referansı
description: OdsoRecipientData mülk. Adres mektup birleştirme gerçekleştirildiğinde veri kaynağındaki kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değerdoğru .
type: docs
weight: 20
url: /tr/net/aspose.words.settings/odsorecipientdata/active/
---
## OdsoRecipientData.Active property

Adres mektup birleştirme gerçekleştirildiğinde veri kaynağındaki kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer`doğru` .

```csharp
public bool Active { get; set; }
```

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

* class [OdsoRecipientData](../)
* ad alanı [Aspose.Words.Settings](../../odsorecipientdata/)
* toplantı [Aspose.Words](../../../)


