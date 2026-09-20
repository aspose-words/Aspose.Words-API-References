---
title: "Aspose::Words::Bibliography::PersonCollection::RemoveAt метод"
linktitle: "RemoveAt"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Bibliography::PersonCollection::RemoveAt метод. Удаляет лицо по указанному индексу в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection::RemoveAt method


Удаляет лицо по указанному индексу.

```cpp
void Aspose::Words::Bibliography::PersonCollection::RemoveAt(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс (нумерация с нуля) лица, которого нужно удалить. |

## Примеры



Показывает, как работать с коллекцией персон.
```cpp
// Создайте новую коллекцию персон.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Добавьте нового человека в коллекцию.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Удалите человека из коллекции, если он существует.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Создайте коллекцию персон с двумя людьми.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Удалить лицо из коллекции по индексу.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Удалить всех лиц из коллекции.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## См. также

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
