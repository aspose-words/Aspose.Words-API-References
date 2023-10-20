---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.OdsoRecipientDataCollection sınıf. Yazılı bir koleksiyonOdsoRecipientData C#'da.
type: docs
weight: 5940
url: /tr/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

Yazılı bir koleksiyon[`OdsoRecipientData`](../odsorecipientdata/)

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Bu koleksiyondaki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | Bu koleksiyonun sonuna bir nesne ekler. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Bu koleksiyondaki tüm öğeleri kaldırır. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | Belirtilen dizindeki öğeyi kaldırır. |

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

* class [OdsoRecipientData](../odsorecipientdata/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
