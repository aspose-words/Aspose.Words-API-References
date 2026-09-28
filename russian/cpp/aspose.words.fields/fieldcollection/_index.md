---
title: "класс Aspose::Words::Fields::FieldCollection"
linktitle: "FieldCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Fields::FieldCollection. Коллекция объектов Field, представляющая поля в указанном диапазоне. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


Коллекция объектов [Field](../field/), представляющая поля в указанном диапазоне. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Удаляет все поля этой коллекции из документа и из самой коллекции. |
| [get_Count](./get_count/)() | Возвращает количество полей в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает поле по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Удаляет указанное поле из этой коллекции и из документа. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет поле по указанному индексу из этой коллекции и из документа. |
| static [Type](./type/)() |  |
## Примечания


Экземпляр этой коллекции перебирает поля, которые находятся в указанном диапазоне.

Коллекция [FieldCollection](./) не владеет содержащимися в ней полями, а лишь представляет их выборку.

Коллекция [FieldCollection](./) является «живой», то есть изменения дочерних элементов объектa‑узла, из которого она была создана, немедленно отражаются в полях, возвращаемых свойствами и методами [FieldCollection](./).

## Примеры



Показывает, как удалять поля из коллекции полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Ниже представлены четыре способа удаления полей из коллекции полей.
// 1 -  Получить поле, которое удалит себя:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Получить коллекцию, чтобы удалить поле, которое мы передаём её методу удаления:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Удалить поле из коллекции по индексу:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Удалить все поля из коллекции сразу:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
