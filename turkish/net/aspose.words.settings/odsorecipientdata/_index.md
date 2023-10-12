---
title: Class OdsoRecipientData
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.OdsoRecipientData sınıf. Dış veri kaynağı içindeki adresmektup birleştirmenin dışında tutulacak tek bir kayıt hakkındaki bilgileri temsil eder.
type: docs
weight: 5930
url: /tr/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Dış veri kaynağı içindeki adres-mektup birleştirmenin dışında tutulacak tek bir kayıt hakkındaki bilgileri temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class OdsoRecipientData
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Adres-mektup birleştirme gerçekleştirilirken veri kaynağındaki kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer:`doğru` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Geçerli kayıt için benzersiz verileri içeren veri kaynağı içindeki sütunu belirtir. Varsayılan değer 0. 'dir |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word kullanır[`Hash`](./hash/) bir kayıt yerine tüm bir kaydın[`UniqueTag`](./uniquetag/) değer. Varsayılan değer 0. 'dir |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Benzersiz verileri içeren sütundaki belirli bir kaydın içeriğini belirtir. Varsayılan değer:`hükümsüz` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Bu nesnenin derin bir kopyasını döndürür. |

### Notlar

Bir kaydın birleştirilmiş bir belge halinde birleştirilmesi durumunda o kayda ilişkin herhangi bir bilgiye ihtiyaç duyulmaz. Bununla birlikte, belirli bir kayıt birleştirilmiş bir belgede birleştirilmeyecekse, bu kayıt için benzersiz anahtarının değeri,[`UniqueTag`](./uniquetag/)Bu hariç tutmayı belirtmek için bu nesnenin özelliği.

### Örnekler

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


