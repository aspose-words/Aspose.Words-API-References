---
title: PersonCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: PersonCollection Remove yöntemiyle koleksiyonunuzdan bir kişiyi zahmetsizce kaldırın. Veri yönetiminizi bugün kolaylaştırın!
type: docs
weight: 70
url: /tr/net/aspose.words.bibliography/personcollection/remove/
---
## PersonCollection.Remove method

Kişiyi koleksiyondan kaldırır.

```csharp
public bool Remove(Person person)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| person | Person | Koleksiyondan çıkarılacak kişi. |

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

* class [Person](../../person/)
* class [PersonCollection](../)
* ad alanı [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* toplantı [Aspose.Words](../../../)
