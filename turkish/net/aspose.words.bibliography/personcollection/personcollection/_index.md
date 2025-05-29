---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: .NET için Aspose.Words
description: PersonCollection sınıfıyla dinamik bir birey koleksiyonu oluşturun ve yönetin. Veri işlemeyi basitleştirin ve uygulamalarınızı bugün geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

Yeni bir örneğini başlat[`PersonCollection`](../) sınıf.

```csharp
public PersonCollection()
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

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### Ayrıca bakınız

* class [Person](../../person/)
* class [PersonCollection](../)
* ad alanı [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* toplantı [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

Yeni bir örneğini başlat[`PersonCollection`](../) sınıf.

```csharp
public PersonCollection(params Person[] persons)
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

* class [Person](../../person/)
* class [PersonCollection](../)
* ad alanı [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* toplantı [Aspose.Words](../../../)
