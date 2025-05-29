---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: PersonCollection Add yöntemi ile koleksiyonunuza zahmetsizce bir Kişi ekleyin. Veri yönetimini kolaylaştırın ve projenizin verimliliğini artırın!
type: docs
weight: 40
url: /tr/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Bir tane ekler[`Person`](../../person/) koleksiyona.

```csharp
public void Add(Person person)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| person | Person | Koleksiyona eklenecek kişi. |

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
