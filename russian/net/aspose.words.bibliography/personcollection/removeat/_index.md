---
title: PersonCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words для .NET
description: Легко используйте метод PersonCollection RemoveAt для удаления персоны по индексу, оптимизируя управление данными с легкостью и точностью.
type: docs
weight: 80
url: /ru/net/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection.RemoveAt method

Удаляет человека по указанному индексу.

```csharp
public void RemoveAt(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Нулевой индекс человека, которого необходимо удалить. |

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
