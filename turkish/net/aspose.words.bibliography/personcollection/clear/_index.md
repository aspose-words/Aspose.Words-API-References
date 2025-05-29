---
title: PersonCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: .NET için Aspose.Words
description: KişiKoleksiyonunuzu Clear yöntemimizle zahmetsizce temizleyin, yeni bir başlangıç için tüm öğeleri anında kaldırın. Veri yönetiminizi bugün basitleştirin!
type: docs
weight: 50
url: /tr/net/aspose.words.bibliography/personcollection/clear/
---
## PersonCollection.Clear method

Koleksiyondaki tüm öğeleri kaldırır.

```csharp
public void Clear()
```

## Örnekler

Kişi koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
// Yeni bir kişi koleksiyonu oluştur.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Koleksiyona yeni kişi ekle.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Eğer varsa kişiyi koleksiyondan kaldır.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// İki kişiden oluşan kişi koleksiyonu oluştur.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Kişiyi dizine göre koleksiyondan kaldır.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Koleksiyondan tüm kişileri kaldır.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Ayrıca bakınız

* class [PersonCollection](../)
* ad alanı [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* toplantı [Aspose.Words](../../../)
