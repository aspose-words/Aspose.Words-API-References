---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words для .NET
description: Создавайте и управляйте динамической коллекцией лиц с помощью класса PersonCollection. Упростите обработку данных и улучшите свои приложения уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

Инициализирует новый экземпляр[`PersonCollection`](../) класс.

```csharp
public PersonCollection()
```

## Примеры

Показывает, как работать с коллекцией персон.

```csharp
// Создать новую коллекцию персон.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Добавить нового человека в коллекцию.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Удалить человека из коллекции, если он существует.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Создать коллекцию из двух человек.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Удалить человека из коллекции по индексу.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Удалить всех людей из коллекции.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Смотрите также

* class [PersonCollection](../)
* пространство имен [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* сборка [Aspose.Words](../../../)

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### Смотрите также

* class [Person](../../person/)
* class [PersonCollection](../)
* пространство имен [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* сборка [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

Инициализирует новый экземпляр[`PersonCollection`](../) класс.

```csharp
public PersonCollection(params Person[] persons)
```

## Примеры

Показывает, как работать с коллекцией персон.

```csharp
// Создать новую коллекцию персон.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Добавить нового человека в коллекцию.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Удалить человека из коллекции, если он существует.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Создать коллекцию из двух человек.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Удалить человека из коллекции по индексу.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Удалить всех людей из коллекции.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Смотрите также

* class [Person](../../person/)
* class [PersonCollection](../)
* пространство имен [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* сборка [Aspose.Words](../../../)
