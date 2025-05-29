---
title: OdsoRecipientData Class
linktitle: OdsoRecipientData
articleTitle: OdsoRecipientData
second_title: .NET için Aspose.Words
description: Verimli belge işleme için posta birleştirmelerinde belirli kayıtları yönetmek ve hariç tutmak üzere tasarlanmış Aspose.Words.Settings.OdsoRecipientData sınıfını keşfedin.
type: docs
weight: 6760
url: /tr/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Posta birleştirmeden hariç tutulacak harici bir veri kaynağındaki tek bir kayıtla ilgili bilgileri temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

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
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Posta birleştirme işlemi gerçekleştirildiğinde veri kaynağındaki kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer:`doğru` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Geçerli kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. Varsayılan değer 0'dır. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word kullanır[`Hash`](./hash/) bir kaydın tamamı yerine[`UniqueTag`](./uniquetag/) değer. Varsayılan değer 0. 'dir |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Benzersiz verileri içeren sütundaki belirli bir kaydın içeriğini belirtir. Varsayılan değer:`hükümsüz` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Bu nesnenin derin bir klonunu döndürür. |

## Notlar

Bir kayıt birleştirilmiş bir belgeye birleştirilecekse, o kayıt hakkında hiçbir bilgiye gerek yoktur. Ancak, belirli bir kayıt birleştirilmiş bir belgeye birleştirilmeyecekse, o kayda ait benzersiz anahtar değeri,[`UniqueTag`](./uniquetag/)Bu dışlamayı belirtmek için bu nesnenin özelliği.

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
